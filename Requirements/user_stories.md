# User Stories — University Library Management System (LMS)

**Project Name:** `university-library-management-system`

## 1. Overview

This document lists **8 core user stories** for our Library Management System. Each user story uses the standard format:  
> **"As a [type of user], I want [some feature], so that [some benefit or goal]."**

---

## 2. Summary Table of User Stories

| ID | As a... | I want to... | So that I can... |
| :-: | :--- | :--- | :--- |
| **US-01** | Student | Search for books by title, author, or category | Quickly check if a book is available before visiting the library. |
| **US-02** | Student | Reserve a book that is currently checked out | Get placed on a waiting list and receive priority when it is returned. |
| **US-03** | Student | View my current active loans and due dates | Return books on time and avoid paying late fines. |
| **US-04** | Faculty Member | Borrow up to 10 books with longer due dates | Keep research materials for 30 days without frequent renewals. |
| **US-05** | Librarian | Issue (check out) a book to a member using their ID | Fast and accurately track physical book movements at the desk. |
| **US-06** | Librarian | Process returned books and automatically calculate fines | Save time on manual math and update the book's status instantly. |
| **US-07** | Librarian | Add, update, or remove book records in the catalog | Keep the library database accurate and up to date for all users. |
| **US-08** | Library Admin | Generate monthly reports on borrowed books and total fines | See library usage data and make better decisions for buying new books. |

---

## 3. Detailed User Stories

### US-01: Book Search
* **User Story:** As a **Student**, I want to search for books by title, author, or category, so that I can quickly check if a book is available before visiting the library.
* **Why It Matters:** Helps students save time by checking availability online first.

### US-02: Book Reservation
* **User Story:** As a **Student**, I want to reserve a book that is currently checked out, so that I can get placed on a waiting list and receive priority when it is returned.
* **Why It Matters:** Gives students a fair First-In, First-Out (FIFO) queue for popular books.

### US-03: View Active Loans & Due Dates
* **User Story:** As a **Student**, I want to view my active loans and due dates on my personal dashboard, so that I can return books on time and avoid paying late fines.
* **Why It Matters:** Gives students clear visibility over their borrowed items and due dates.

### US-04: Faculty Extended Borrowing
* **User Story:** As a **Faculty Member**, I want to borrow up to 10 books for a longer duration (30 days), so that I can keep research materials for teaching without frequent renewals.
* **Why It Matters:** Supports university professors with their extended academic research needs.

### US-05: Librarian Counter Check-Out
* **User Story:** As a **Librarian**, I want to issue a book to a student using their Student ID, so that I can fast and accurately track physical book check-outs at the desk.
* **Why It Matters:** Reduces counter waiting lines and replaces manual paper logbooks.

### US-06: Book Return & Automated Fines
* **User Story:** As a **Librarian**, I want to process returned books and let the system calculate overdue fines automatically, so that I can save time on manual math and update book status instantly.
* **Why It Matters:** Avoids human calculation mistakes and automatically charges $0.50/day for late returns.

### US-07: Catalog Inventory Management
* **User Story:** As a **Librarian**, I want to add, update, or remove book records in the catalog, so that I can keep the library inventory accurate and up to date.
* **Why It Matters:** Ensures users are always viewing the latest library catalog information.

### US-08: Admin Usage Reports
* **User Story:** As a **Library Admin**, I want to generate monthly reports on borrowed books and collected fines, so that I can see library usage data and make better decisions for buying new books.
* **Why It Matters:** Helps library management understand reader trends and track fine revenue.

---

## 4. Final Submission Checklist

* [x] Exactly 8 clear user stories covering all 4 key stakeholders (Student, Faculty, Librarian, Admin).
* [x] Strictly follows the standard "As a..., I want..., so that..." format.
* [x] Written in simple, easy-to-explain language for class presentation.
* [x] Ready to save directly into `requirements/user-stories.md` on GitHub.