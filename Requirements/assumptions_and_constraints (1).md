# System Assumptions & Constraints

**Project Name:** `university-library-management-system`

## 1. Quick Summary

This document lists the main **Assumptions** (things we expect to be true) and **Constraints** (rules or limits we must follow) for our University Library Management System (LMS).

| \# | Title | Type | What It Means | 
| ----- | ----- | ----- | ----- | 
| **1** | No Full Software Code | Constraint | We only create reports, diagrams, and UI designs, not full backend code. | 
| **2** | No Special Hardware or Real Money | Constraint | We do not use real barcode scanners or real online payment methods. | 
| **3** | Time & Team Limits | Constraint | All work must finish within the 12-week semester schedule. | 
| **4** | Users Have Internet & Accounts | Assumption | Students and teachers have active university accounts and internet access. | 
| **5** | Accurate Library Data | Assumption | Book lists, member details, and fine rates stored in the system are correct. | 

## 2. System Constraints (Rules We Must Follow)

### Constraint 1: Documentation & Design Only (No Implementation)

* **Explanation:** According to the assignment guidelines, our task is to analyze the problem, write requirements, draw UML diagrams, make Figma screen designs, and manage our work on GitHub.

* **Result:** We do not need to write complete backend software code.

### Constraint 2: No Physical Hardware or Real Payment Systems

* **Explanation:** Our web project does not connect to real physical equipment or real bank accounts.

* **Exclusions:**

  * **No Hardware:** No real RFID gates or barcode scanners.

  * **No Real Money:** No actual credit card or online payment handling.

* **Result:** Overdue fines and book entries will be tested using simple web screens.

### Constraint 3: Fixed Project Timeline and Schedule

* **Explanation:** All project work must be completed within the 12-week semester deadline across all project phases (requirements, diagrams, UI design, and reporting).

## 3. System Assumptions (Things We Expect to Be True)

### Assumption 1: Users Have University Logins & Devices

* **Explanation:** We assume all students, faculty members, and librarians have active university username/passwords and access to a smartphone or computer with a web browser.

* **Result:** We only need to design a standard web login screen instead of building a new user registration system from scratch.

### Assumption 2: Correct Data & System Rules

* **Explanation:** We assume that student details, book titles, and library rules (like fine rates and loan limits) in the database are correct.

* **Result:** This allows our system features—such as fine calculations ($0.50/day), borrowing limits (Students: 3 books, Faculty: 10 books), and waiting queues (FIFO)—to work smoothly.

## 4. Final Submission Checklist

* \[x\] Covers all 5 main assumptions and constraints.

* \[x\] Written in simple, easy-to-explain language.

* \[x\] Ready to upload to the `requirements/` folder on GitHub.