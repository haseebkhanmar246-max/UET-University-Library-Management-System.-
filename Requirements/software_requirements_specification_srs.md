# Software Requirements Specification (SRS)
## University Library Management System (LMS)

**Project Name:** `university-library-management-system`  
**Document Version:** 1.0  
**Status:** Ready for Submission  

---

## Revision History

| Version | Date | Author / Role | Summary of Changes |
| :---: | :---: | :--- | :--- |
| **0.1** | Nov 2026 | Analysis Team | Initial draft of stakeholder needs, assumptions, and constraints. |
| **0.5** | Nov 2026 | Analysis Team | Added user stories, acceptance criteria, and functional/non-functional requirements. |
| **1.0** | Nov 25, 2026 | Analysis Team | Finalized full SRS with Table of Contents, numbered requirements, and revision history. |

---

## Table of Contents

1. [Introduction](#1-introduction)
   - 1.1 [Purpose](#11-purpose)
   - 1.2 [Scope](#12-scope)
   - 1.3 [Definitions & Acronyms](#13-definitions--acronyms)
2. [Overall Description](#2-overall-description)
   - 2.1 [Stakeholders & User Roles](#21-stakeholders--user-roles)
   - 2.2 [Assumptions & Constraints](#22-assumptions--constraints)
3. [User Stories & Acceptance Criteria](#3-user-stories--acceptance-criteria)
4. [Specific Requirements](#4-specific-requirements)
   - 4.1 [Functional Requirements](#41-functional-requirements)
   - 4.2 [Non-Functional Requirements](#42-non-functional-requirements)
5. [Requirements Traceability Summary](#5-requirements-traceability-summary)

---

## 1. Introduction

### 1.1 Purpose
This Software Requirements Specification (SRS) describes what the **University Library Management System (LMS)** must do and the quality standards it must meet. It serves as a clear reference for design diagrams, UI prototypes, and team reviews.

### 1.2 Scope
The LMS is a web-based system that supports catalog searching, book borrowing and returns, First-In, First-Out (FIFO) reservations, overdue fine calculation, role-based access, and usage reporting. Physical hardware integration (like barcode scanners), live online payment processing, and full backend code implementation are outside the scope of this assignment.

### 1.3 Definitions & Acronyms
* **LMS:** Library Management System
* **SRS:** Software Requirements Specification
* **FIFO:** First-In, First-Out (the first user to reserve a book gets priority when it returns)
* **RBAC:** Role-Based Access Control (permissions based on user role)
* **FR:** Functional Requirement
* **NFR:** Non-Functional Requirement

---

## 2. Overall Description

### 2.1 Stakeholders & User Roles
* **Librarian:** Manages book records, issues and returns books at the desk, and handles overdue fines.
* **Student:** Searches books, checks availability, places reservations, and views loans and due dates.
* **Faculty Member:** Searches academic resources and borrows books with extended limits and loan periods.
* **Library Administrator:** Manages user accounts, enforces library rules, and generates summary reports.

### 2.2 Assumptions & Constraints
* **C-01 (No Full Implementation):** Deliverables focus on analysis, SRS, diagrams, and UI prototypes rather than complete production code.
* **C-02 (No Hardware or Live Payments):** No physical scanning hardware or live payment gateways are used; fine handling is simulated on web screens.
* **C-03 (Academic Schedule):** All work must be completed within the semester timeline.
* **A-01 (Accounts & Browsers):** Users have valid university accounts and access the web interface via standard browsers.
* **A-02 (Accurate Core Data):** Book records, user details, and library fine/loan rules in the system are accurate.

---

## 3. User Stories & Acceptance Criteria

* **US-01 (Book Search):** As a **Student**, I want to search for books by title, author, or category, so that I can quickly check if a book is available before visiting the library.  
  * *Acceptance Criteria:* Results appear in under 2–3 seconds and show title, author, ISBN, category, and availability status.
* **US-02 (Book Reservation):** As a **Student**, I want to reserve a book that is currently checked out, so that I can get placed on a waiting list and receive priority when it is returned.  
  * *Acceptance Criteria:* System places the student in a FIFO queue and holds a returned book for 48 hours for the next user in line.
* **US-03 (View Loans & Due Dates):** As a **Student**, I want to view my current active loans and due dates, so that I can return books on time and avoid paying late fines.  
  * *Acceptance Criteria:* Dashboard lists borrowed items, loan dates, due dates, and fines, highlighting items due within 2 days.
* **US-04 (Faculty Borrowing):** As a **Faculty Member**, I want to borrow up to 10 books with longer due dates, so that I can keep research materials for 30 days without frequent renewals.  
  * *Acceptance Criteria:* System allows up to 10 active loans and sets a 30-day due date for faculty accounts (compared to 3 books and 14 days for students).
* **US-05 (Counter Check-Out):** As a **Librarian**, I want to issue a book to a member using their ID, so that I can fast and accurately track physical book check-outs at the desk.  
  * *Acceptance Criteria:* Check-out completes quickly (under 3 seconds), sets the due date, and updates book availability to checked out.
* **US-06 (Returns & Fines):** As a **Librarian**, I want to process returned books and automatically calculate fines, so that I can save time on manual math and update the book's status instantly.  
  * *Acceptance Criteria:* Overdue days are multiplied by the fine rate (e.g., $0.50/day), added to the user's fine balance, and book availability is updated.
* **US-07 (Catalog Management):** As a **Librarian**, I want to add, update, or remove book records in the catalog, so that I can keep the library database accurate and up to date.  
  * *Acceptance Criteria:* Required fields are validated, duplicate ISBNs are blocked with an error message, and changes appear in the catalog.
* **US-08 (Admin Reports):** As a **Library Admin**, I want to generate monthly reports on borrowed books and total fines, so that I can see library usage data and make better decisions for buying new books.  
  * *Acceptance Criteria:* Report summarizes books, users, check-outs, returns, overdue items, and fines, and can be exported within 5 seconds.

---

## 4. Specific Requirements

### 4.1 Functional Requirements

| Req. ID | Requirement Description |
| :---: | :--- |
| **FR-01** | The system shall allow the librarian to add new books by entering details such as title, author, ISBN, category, and quantity. |
| **FR-02** | The system shall allow the librarian to update or delete existing book records. |
| **FR-03** | The system shall allow students and faculty members to search for books by title, author, ISBN, or category. |
| **FR-04** | The system shall display book details and availability status in search results. |
| **FR-05** | The system shall allow the librarian to issue available books to registered students and faculty members. |
| **FR-06** | The system shall record book issue dates and due dates for every borrowed book. |
| **FR-07** | The system shall allow the librarian to record returned books and update their availability status. |
| **FR-08** | The system shall allow users to view their currently borrowed books, due dates, and borrowing history. |
| **FR-09** | The system shall identify overdue books and calculate fines according to the library's fine rules. |
| **FR-10** | The system shall allow users to reserve a book that is currently unavailable using a FIFO queue. |
| **FR-11** | The system shall allow the administrator to create, update, and manage student, faculty, and librarian accounts. |
| **FR-12** | The system shall allow the administrator to generate reports about books, registered users, issued books, returned books, and overdue books. |

### 4.2 Non-Functional Requirements

| Req. ID | Category | Requirement Description |
| :---: | :---: | :--- |
| **NFR-01** | Performance | The system should display search results within 3 seconds under normal operating conditions. |
| **NFR-02** | Security | The system shall require users to log in with valid credentials and restrict access according to their roles. |
| **NFR-03** | Reliability | The system should store and process library records accurately and protect data from loss through regular backups. |
| **NFR-04** | Usability | The system should provide a simple, clear, and user-friendly interface so students, faculty members, librarians, and administrators can use it easily. |

---

## 5. Requirements Traceability Summary

| User Story | Related Functional Reqs. | Related Non-Functional Reqs. | Primary Role |
| :---: | :---: | :---: | :--- |
| **US-01** | FR-03, FR-04 | NFR-01 | Student / Faculty |
| **US-02** | FR-10 | NFR-03 | Student |
| **US-03** | FR-06, FR-08 | NFR-04 | Student |
| **US-04** | FR-05, FR-06 | NFR-02 | Faculty Member |
| **US-05** | FR-05, FR-06 | NFR-01 | Librarian |
| **US-06** | FR-07, FR-09 | NFR-03 | Librarian |
| **US-07** | FR-01, FR-02 | NFR-03 | Librarian |
| **US-08** | FR-11, FR-12 | NFR-02 | Library Admin |