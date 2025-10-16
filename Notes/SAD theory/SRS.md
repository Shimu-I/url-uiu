# 📄 Software Requirement Specification (SRS) – CSE3411 (Content 7)

## 🎯 Definition
> A Software Requirement Specification (SRS) is a formal document describing the software’s purpose, features, functions, and constraints — acting as a contract between developer and client.

---

## 🧩 Purpose of SRS
- Defines **scope** and **objectives**.  
- Serves as a **baseline** for design, testing, and maintenance.  
- Ensures **common understanding** among stakeholders.  
- Prevents **scope creep** and misunderstandings.

---

## 🧱 Structure of an SRS

| Section | Description |
|----------|-------------|
| **Purpose** | Why the document exists. |
| **Scope** | What the software aims to achieve. |
| **Overview** | Description of product and goals. |
| **Functional Requirements** | Actions the system must perform. |
| **Interface Requirements** | Interactions between components/users. |
| **Performance Requirements** | Speed, load time, capacity expectations. |
| **Design Constraints** | Technical or regulatory limitations. |
| **Non-Functional Attributes** | Usability, Security, Reliability, Maintainability. |
| **Preliminary Schedule & Budget** | Initial plan and resource outline. |

---

## ⚙️ Functional vs Non-Functional Requirements

| Type | Description | Example |
|------|--------------|----------|
| **Functional** | What the system *does*. | Login, Register, Search, Report generation |
| **Non-Functional** | How well the system performs. | Security, Performance, Reliability |

---

## 🧪 Validation of SRS
Ensures the document is **Complete** and **Correct** before development.

### Common Errors:
1. **Omission** – Missing requirements.  
2. **Inconsistency** – Contradictory statements.  
3. **Incorrect Facts** – False data.  
4. **Ambiguity** – Multiple meanings.

---

## 🧠 Characteristics of a Good SRS

| Property | Description | Example |
|-----------|--------------|----------|
| **Correctness** | Reflects true user needs. | Report frequency matches actual need. |
| **Completeness** | All use cases covered. | Login includes valid/invalid flow. |
| **Consistency** | No contradictions. | Same password rule everywhere. |
| **Unambiguity** | One interpretation only. | “Load in 3s” not “fast”. |
| **Modifiability** | Easy to update. | Numbered, modular requirements. |
| **Traceability** | Each requirement linked to origin. | REQ-15 → user story. |
| **Verifiability** | Can be tested objectively. | “Handles 500 users.” |
| **Testability** | Allows test case creation. | 1000 transactions/sec. |
| **Comprehensibility** | Easy to read & understand. | Plain, clear language. |
| **Feasibility** | Technically & financially realistic. | 3s load time feasible. |

---

## 🧩 3C Properties in SRS

| Property | Meaning |
|-----------|----------|
| **Completeness** | Includes all necessary requirements. |
| **Correctness** | Accurately reflects what the client wants. |
| **Consistency** | No conflicting or contradictory requirements. |

---

## 🧾 Using SRS in Exam Answers

### 🔸 For “Define/Explain 3C”
> A good SRS must be **Complete, Correct, and Consistent**, ensuring full coverage, accuracy, and harmony of requirements.

### 🔸 For “Functional/Non-Functional Requirements”
> Functional: Login, Registration, Payment.  
> Non-Functional: Performance, Security, Usability.

### 🔸 For “SRS as Blueprint”
> Acts as a master reference for developers, testers, and managers — a shared vision of what the final product must achieve.

---

## 📌 Quick Summary
✅ Focus: *3C Properties, Functional vs Non-Functional, Validation*  
✅ Apply: *Characteristics of good SRS + Common Errors*  
✅ Example Topics: UCAM, HealthHub, SecureLocker, CampusRide
