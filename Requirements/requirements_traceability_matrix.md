# Requirements Traceability Matrix (RTM)

**Project Name:** `university-library-management-system`

## 1. Overview

The **Requirements Traceability Matrix (RTM)** connects each project requirement back to its original stakeholder, corresponding user story, functional requirement, non-functional requirement, and acceptance criteria. This ensures that no feature is missed and every system module directly satisfies a documented user need.

---

## 2. Requirements Traceability Table

| Stakeholder Role | User Story ID | Functional Req. (FR) | Non-Functional Req. (NFR) | Acceptance Criteria ID | Verification Status |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Student / Faculty** | `US-01` | **FR-03, FR-04** | NFR-01 *(Performance < 3s)* | `AC-01` | ✅ Verified |
| **Student** | `US-02` | **FR-10** | NFR-03 *(Data Reliability)* | `AC-02` | ✅ Verified |
| **Student** | `US-03` | **FR-06, FR-08** | NFR-04 *(Usability)* | `AC-03` | ✅ Verified |
| **Faculty Member** | `US-04` | **FR-05, FR-06** | NFR-02 *(RBAC Security)* | `AC-04` | ✅ Verified |
| **Librarian** | `US-05` | **FR-05, FR-06** | NFR-01 *(Performance < 3s)* | `AC-05` | ✅ Verified |
| **Librarian** | `US-06` | **FR-07, FR-09** | NFR-03 *(Reliable Fine Math)* | `AC-06` | ✅ Verified |
| **Librarian** | `US-07` | **FR-01, FR-02** | NFR-03 *(Catalog Integrity)* | `AC-07` | ✅ Verified |
| **Library Admin** | `US-08` | **FR-11, FR-12** | NFR-02 *(Admin Security)* | `AC-08` | ✅ Verified |

---

## 3. Mapping Breakdown by Requirement ID

### 1. Catalog & Search Management
* **FR-01 & FR-02 (Catalog Management):** Traced to **Librarian** via `US-07` and verified by `AC-07`.
* **FR-03 & FR-04 (Book Search & Status):** Traced to **Student/Faculty** via `US-01`, guided by `NFR-01` (search performance), and verified by `AC-01`.

### 2. Circulation & Reservation Management
* **FR-05 & FR-06 (Issue Book & Due Dates):** Traced to **Librarian & Faculty** via `US-04` & `US-05`, guarded by `NFR-02` (Role-Based Access Control), and verified by `AC-04` & `AC-05`.
* **FR-07 (Return Book Processing):** Traced to **Librarian** via `US-06` and verified by `AC-06`.
* **FR-10 (FIFO Reservations):** Traced to **Student** via `US-02`, supported by `NFR-03` (Reliability), and verified by `AC-02`.

### 3. Fines, History & Administration
* **FR-08 (User Loans & History):** Traced to **Student** via `US-03`, supported by `NFR-04` (Usability), and verified by `AC-03`.
* **FR-09 (Overdue Fine Calculation):** Traced to **Librarian** via `US-06` and verified by `AC-06`.
* **FR-11 & FR-12 (Account & Report Management):** Traced to **Library Admin** via `US-08`, secured by `NFR-02` (Security), and verified by `AC-08`.

---

## 4. Final Submission Checklist

- [x] Maps all 4 Stakeholders (Student, Faculty, Librarian, Admin).
- [x] Includes all 8 User Stories (`US-01` to `US-08`).
- [x] Covers all 12 Functional Requirements (`FR-01` to `FR-12`).
- [x] Links all 4 Non-Functional Requirements (`NFR-01` to `NFR-04`).
- [x] Aligns with Acceptance Criteria (`AC-01` to `AC-08`).
- [x] Ready to save directly to `requirements/traceability-matrix.md` on GitHub.