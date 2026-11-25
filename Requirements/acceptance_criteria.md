# Acceptance Criteria — University Library Management System (LMS)

**Project Name:** `university-library-management-system`

## 1. Overview

This document outlines the **measurable acceptance criteria** for each of the 8 user stories. Acceptance criteria define the exact conditions that must be met for a user story to be considered complete and working correctly.

---

## 2. Measurable Acceptance Criteria List

### US-01: Book Search
* **Given** a user opens the catalog search page,
* **When** they type a search term (Title, Author, ISBN, or Category) and press search,
* **Then** the system displays matching search results in **under 2 seconds**.
* **And** each result clearly shows the book title, author, ISBN, category, and real-time status (**Available** or **Checked Out**).

---

### US-02: Book Reservation
* **Given** a book is currently marked as "Checked Out",
* **When** an logged-in student clicks the "Reserve Book" button,
* **Then** the system adds the student to the First-In, First-Out (FIFO) waiting queue and shows a success message.
* **And** when the book is returned, the system holds the book exclusively for that student for **48 hours** before offering it to anyone else.

---

### US-03: View Active Loans & Due Dates
* **Given** a student is logged into their personal dashboard,
* **When** they open the "My Borrowed Books" section,
* **Then** the system lists all their currently borrowed books, loan dates, exact due dates, and any active fine balance.
* **And** any book due within **2 days** is clearly highlighted in yellow/red as an urgent warning.

---

### US-04: Faculty Extended Borrowing
* **Given** a user logged in with the "Faculty" role,
* **When** a librarian issues a book to their account,
* **Then** the system automatically sets the loan duration to **30 days** (instead of 14 days for students).
* **And** allows the faculty member to hold up to **10 books** at the same time without triggering a limit error.

---

### US-05: Librarian Counter Check-Out
* **Given** a librarian is on the Check-Out counter page,
* **When** they enter a valid Student ID and Book ISBN and click "Issue Book",
* **Then** the system completes the transaction in **under 3 seconds**.
* **And** automatically updates the book status from "Available" to "Checked Out" while reducing the available copy count by 1.

---

### US-06: Book Return & Automated Fines
* **Given** a book is being returned past its due date,
* **When** the librarian processes the return in the system,
* **Then** the system automatically calculates the fine at **$0.50 per day overdue**.
* **And** immediately adds the calculated amount to the user's account fine balance while updating the book status back to "Available".

---

### US-07: Catalog Inventory Management
* **Given** a librarian wants to add a new book to the catalog,
* **When** they fill in all required fields (Title, Author, ISBN, Quantity) and click "Save",
* **Then** the system validates that no field is empty and updates the search index immediately.
* **And** if the ISBN already exists, the system shows an error message: *"Duplicate ISBN not allowed."*

---

### US-08: Admin Usage Reports
* **Given** a Library Admin is logged into the reports section,
* **When** they select a date range and click "Generate Report",
* **Then** the system creates a total summary showing total check-outs, active loans, overdue items, and total fines collected.
* **And** provides a button to download the summary report as a **PDF or CSV file within 5 seconds**.

---

## 3. Quick Testability Matrix

| User Story ID | Key Test Metric | Expected Result | Status |
| :---: | :--- | :--- | :---: |
| **US-01** | Search Speed | Results loaded in < 2.0 seconds | Pass |
| **US-02** | Priority Hold | Reserved book held for 48 hours | Pass |
| **US-03** | Dashboard Warning | Highlight due dates within 2 days | Pass |
| **US-04** | Faculty Limit | 10 books max & 30-day return window | Pass |
| **US-05** | Check-Out Speed | Transaction complete in < 3.0 seconds | Pass |
| **US-06** | Fine Math | Overdue days × $0.50 added automatically | Pass |
| **US-07** | Field Validation | Block empty inputs & duplicate ISBNs | Pass |
| **US-08** | Report Export | Downloadable PDF/CSV created in < 5 seconds | Pass |