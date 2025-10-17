### **Q28. Bus Synchronization Problem**

**Question:**

A bus with capacity **K** arrives at a bus stop periodically. It lets up to **K waiting passengers** board and then departs. Passengers arriving after the bus starts boarding must wait for the next bus. You are given:

```bash
mutex = 1
bus_arrived = 0
passenger_boarded = 0
waiting_count = 0

```

Passenger code:

```bash
down(mutex)
waiting_count++
up(mutex)
down(bus_arrived)
board()
up(passenger_boarded)

```

Write the corresponding bus thread.

**Simplified Answer:**

```bash
down(mutex)
N = min(waiting_count, K)
for i = 1 to N:
    up(bus_arrived)          # let one passenger board
    down(passenger_boarded)  # wait until boarded
waiting_count -= N
up(mutex)
depart()

```

**Explanation:**

The bus wakes only as many passengers as it can carry, waits for all to finish boarding, then updates the waiting count and departs.

---

### **Q30. Roller Coaster Ride Problem**

**Question:**

Operator waits for **N riders** to arrive before starting the ride. Once all N riders arrive, he opens the gate and lets them in. After all have entered, the ride starts.

**Simplified Answer (using lock + condition variables):**

```bash
# Variables
int rider_count = 0, enter_count = 0
cond cv_rider, cv_operator1, cv_operator2
mutex m

# Operator
lock(m)
while (rider_count < N):
    wait(cv_operator1, m)
open_ride()
for i in 1..N:
    signal(cv_rider)
while (enter_count < N):
    wait(cv_operator2, m)
start_ride()
unlock(m)

# Rider
lock(m)
rider_count++
if (rider_count == N):
    signal(cv_operator1)
wait(cv_rider, m)
enter_ride()
enter_count++
if (enter_count == N):
    signal(cv_operator2)
unlock(m)

```

**Explanation:**

Riders wait until the operator opens the ride. The last arriving rider signals the operator. After everyone enters, the operator starts the ride.

---

### **Q31. Host–Guest Problem**

**Question:**

The host waits for all **N guests** to arrive before opening the door. Guests must enter **only after** the door is opened.

**Simplified Answer:**

```bash
# Host
lock(m)
while (guest_count < N):
    wait(cv_host, m)
openDoor()
signal(cv_guest)
unlock(m)

# Guest
lock(m)
guest_count++
if (guest_count == N):
    signal(cv_host)
wait(cv_guest, m)
signal(cv_guest)
unlock(m)
enterHouse()

```

**Explanation:**

Each guest waits for all others to arrive. The host opens the door once all guests are present, then signals everyone to enter.

---

### **Q44. Barber Shop Problem**

**Question:**

There’s one barber and **N waiting chairs**.

- If no chairs are free, a customer leaves.
- If barber is asleep, the first arriving customer wakes him.
- Use semaphores only.

**Simplified Answer:**

```bash
# Shared
semaphore mutex = 1, customers = 0, barber = 0
int waiting_count = 0

# Customer
down(mutex)
if (waiting_count == N):
    up(mutex)
    leave()
waiting_count++
up(mutex)
up(customers)
down(barber)
getHairCut()
down(mutex)
waiting_count--
up(mutex)

# Barber
while True:
    down(customers)
    up(barber)
    cutHair()

```

**Explanation:**

The barber sleeps when no customers are waiting. Customers signal when they arrive and wait their turn. The barber cuts hair one at a time.

---

### **Q47. Chocolate Box Problem**

**Question:**

Children eat chocolates from a box of size **N**.

- If empty → a child wakes the mother.
- The mother refills the box with N chocolates.
    
    Use **locks and condition variables**.
    

**Simplified Answer:**

```bash
int count = 0
mutex m
cond fullBox, emptyBox

# Child
while True:
    lock(m)
    while (count == 0):
        signal(emptyBox)
        wait(fullBox, m)
    getChocolateFromBox()
    eat()
    count--
    signal(fullBox)
    unlock(m)

# Mother
while True:
    lock(m)
    while (count > 0):
        wait(emptyBox, m)
    refillChocolateBox(N)
    count = N
    signal_broadcast(fullBox)
    unlock(m)

```

**Explanation:**

Children wait when the box is empty and wake the mother. The mother refills it, signals the children, and they resume eating.

---
