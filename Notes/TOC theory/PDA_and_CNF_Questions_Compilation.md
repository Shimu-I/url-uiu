# 📘 CSE 2233 / CSI 233 – PDA and CNF Questions Compilation

### Organized by Trimester and Year (2022 → 2025)

---

## 🧩 **Fall 2022**
### **CNF Questions**
- Convert the following CFGs into equivalent Chomsky Normal Form (CNF).  
  a)  
  ```
  S → aSBcD | BC
  A → AbCd | a
  B → CBA | ε
  C → c | ε
  D → d
  ```  
  b)  
  ```
  S → xP | yQ | y | RRz
  P → Qxx | xyR | ε
  Q → yPPy | xy | zR
  R → x | y | PR | ε
  ```

### **PDA Questions**
- Draw Push Down Automata (PDA) for the following languages:  
  *(Questions not fully visible in text, possibly included in diagrams)*

---

## 🧩 **Summer 2022**
### **PDA Questions**
- (a) Draw PDA for  
  ```
  L = {a^m b^n c^k | k = m - n and m, n ≥ 1}
  ```
- (b) Draw PDA for  
  ```
  L = {W | W is an Odd Palindrome, W ∈ {0, 1}}
  ```

### **CNF Questions**
- Convert the following CFGs into equivalent CNF.  
  ```
  A → 1 | B | CA | ε
  B → 1BS | 0S0B | ε
  C → x | y | A
  S → 1A1 | 0S | S | A1
  ```  
  and  
  ```
  W → 2XY | 1W | 2Y
  X → 1X3 | 1W3 | ε
  Y → Y11 | 12YW3 | X | ε
  ```

---

## 🧩 **Spring 2023**
### **CNF Questions**
- Convert the given CFGs to Chomsky Normal Form (CNF).  
  *(Three sub-questions, specific rules partially obscured in the image on page 1.)*

### **PDA Questions**
- Draw Push Down Automata (PDA) for the following languages:  
  (a) and (b) – not fully visible but referenced on page 2 of the document.

---

## 🧩 **Fall 2023**
### **CNF Questions**
- Convert the following CFGs into CNF:  
  a)  
  ```
  S → ABC | BaB
  A → aA | BaC | aaa
  C → bBb | a | D
  D → ɛ
  ```
  b)  
  ```
  S → BAC | B
  B → 0B1 | 01
  A → aAb | ε
  C → Bc
  ```

### **PDA Questions**
- Draw the PDA for the following languages:  
  a)  
  ```
  L = { x^m # y^n z^w | m = n/2 or w = m/3, m, n, w > 0 }
  ```  
  b)  
  ```
  L = { a^i b^j c^k | i + j = 2k, i, j, k ≥ 0 }
  ```

---

## 🧩 **Summer 2024**
### **CNF Questions**
- Convert the following grammars into CNF:  
  a)  
  ```
  S → BAC | B
  B → 0B1 | 01
  A → aAb | ε
  C → Bc
  ```
  b)  
  ```
  S → ABA
  A → aA | ε
  B → bBc | ε
  ```

### **PDA Questions**
- Draw the PDA for:  
  a)  
  ```
  L = { x^n y^(3m) z^(2m) v^n | n ≥ 1 }
  ```
  b)  
  ```
  L = { p^i q^j r^k s^m | i = k or m = j + 2, i, j, k, m ≥ 1 }
  ```

---

## 🧩 **Fall 2024**
### **CNF Questions**
- Convert the following grammars into CNF:  
  a)  
  ```
  S → S + S | T - S | S / T | ε
  T → T * TC | C
  C → 0 | 1 | 2 | 3
  ```  
  b)  
  ```
  S → SS | CAB | BA
  A → aAb | ε
  B → 0A1 | 0B1
  C → cA | Bb
  ```

### **PDA Questions**
- Draw the PDA for:  
  a)  
  ```
  L = { x^(3a) y^(2b) z^c w^d | (c = 3b and a = 2d), a ≥ 1, b ≥ 0 }
  ```  
  b)  
  ```
  L = { p^(3i) # q^(2j) r^(2k) | (i = j or i = k), i, j ≥ 1 }
  ```

---

## 🧩 **Spring 2025**
### **CNF Questions**
- Convert the following CFGs into CNF:  
  a)  
  ```
  E → E O E | (E) | (E)(E) | D N
  N → D N | ε
  D → 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
  O → + | − | × | ÷
  ```  
  b)  
  ```
  X → W X W | Y b b
  W → a a | b b
  Y → b a b
  ```

### **PDA Questions**
- Draw the PDA for:  
  a)  
  ```
  L = { x^n # y^(3m) z^(2n) | n ≥ 2, m ≥ 0 }
  ```  
  b)  
  ```
  L = { a^(2p) b^q c^r d^w | q = r/3, w = p + 2, p, q, r ≥ 1 }
  ```

---

✅ **Total Questions Compiled:**  
- CNF: 12 distinct CFG conversion tasks  
- PDA: 10 unique PDA design problems  
