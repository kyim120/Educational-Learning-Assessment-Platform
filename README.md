# Software Requirements Specification (SRS)

## **Project Title:** Online Educational Learning and Assessment Platform

---

## 1. Introduction

### 1.1 Purpose

The purpose of this document is to define the specifications for an online educational platform that provides students access to learning materials, MCQ-based assessments, and chapter or course-based purchasing. The system will offer role-based access for the Owner (Administrator), Content Managers, Finance Manager, and Students.

### 1.2 Scope

The platform will allow students to register, purchase and access course material, take MCQ tests, and download notes and books. The Owner will have full administrative control, including user management, payment plan configuration, and assigning additional managers. The system will integrate with Stripe for online payments.

---

## 2. Overall System Description

The system will be a web-based platform designed to be responsive and accessible on desktop and mobile. It will support payment-based access control, digital content delivery, and structured assessments.

---

## 3. User Roles and Permissions

| Role                  | Description                       | Permissions                                                                                    |
| --------------------- | --------------------------------- | ---------------------------------------------------------------------------------------------- |
| Owner (Administrator) | System Super Admin                | Manage all content, accounts, roles, payment plans, reporting, renewal control                 |
| Content Manager       | Learning material manager         | Add, edit, organize courses, chapters, notes, books, and MCQs                                  |
| Finance Manager       | Accounting and payment controller | View transactions, verify payments, manage student access durations                            |
| Student               | End-user learner                  | Register, purchase content, access permitted study material, attempt tests, view score history |

---

## 4. Functional Requirements

### 4.1 User Authentication

* Students can register, log in, and reset passwords.
* Owner can create and manage Content Managers and Finance Manager accounts.
* Secure session handling is required.

### 4.2 Course and Content Management

* Owner and Content Managers can create course categories and chapters.
* Study materials may include video lectures, text content, downloadable books (PDF), and lecture notes.
* Material access is controlled based on purchased courses or chapters.

### 4.3 Payment and Subscription Access

* Stripe payment integration for online purchasing.
* System records and verifies transactions.
* Finance Manager can manually verify payments if required.
* Owner can update pricing plans at any time.
* Access can be granted on per-chapter or full-course basis.

### 4.4 MCQ Test System

* Content Manager can create MCQs linked to chapters or courses.
* Each MCQ can have between 2 and 9 answer options.
* Correct answers must be securely stored.
* Test system supports scoring, result display, and result history.

### 4.5 Study Materials Library

* Organized collection of notes, books, and lecture content.
* Students can access view/download options based on permissions.
* Reading materials may be streamed online to prevent unauthorized download (optional).

### 4.6 Notifications and Messages

* System emails for registration, payment confirmation, and password recovery.

### 4.7 Reporting and Dashboard

* Owner dashboard includes:

  * Number of registered students
  * Earnings summary
  * Most purchased courses
  * Test performance trends

---

## 5. Non-Functional Requirements

### 5.1 Security

* All user passwords must be encrypted.
* Role-based access control is required.
* System must comply with Stripe security standards.

### 5.2 Performance

* Application should support a minimum of 5,000 active student accounts.
* Page load time must ideally remain below 4 seconds.

### 5.3 Reliability and Backup

* System must auto-backup database daily.
* Availability goal: 99% uptime.

### 5.4 Usability

* User interface must be clean and navigable.
* Responsive design must support desktop and mobile devices.

---

## 6. Technology Stack (Recommended)

| Layer           | Technology                         |
| --------------- | ---------------------------------- |
| Frontend        | React.js / Next.js + Tailwind CSS  |
| Backend         | Node.js (Express) or Laravel (PHP) |
| Database        | MySQL or MongoDB                   |
| Payment Gateway | Stripe                             |
| Authentication  | JWT-based or Session-based Auth    |
| Deployment      | VPS/Cloud Linux Hosting            |

---

## 7. Project Timeline

| Phase                         | Duration |
| ----------------------------- | -------- |
| Requirements & Design         | 1 Week   |
| Backend Development           | 2 Weeks  |
| Frontend Development          | 2 Weeks  |
| Testing & Revisions           | 1 Week   |
| Deployment & Training         | 2–3 Days |
| **Total Duration:**           | 5–6 Weeks|

---

## 8. Budget Breakdown (Base System: PKR 150,000)

| Component                        | Cost       |
| -------------------------------- | ---------- |
| Backend and Database Development | 60,000 PKR |
| Frontend UI/UX Implementation    | 50,000 PKR |
| Payment Integration (Stripe)     | 15,000 PKR |
| Testing and Optimization         | 15,000 PKR |
| Deployment and Configuration     | 10,000 PKR |

---

## 9. Additional Cost for MCQ Options Expansion

The system will support up to 9 answer options per MCQ.
If dynamic MCQ option entry beyond standard formats requires custom UI handling and database expansion:

| Feature                                      | Additional Cost |
| -------------------------------------------- | --------------- |
| Support for MCQs with up to 9 answer options | 3,000 PKR       |

---


## 10. Optional Future Enhancements and Estimated Costs

| Feature                              | Description                                                                                     | Estimated Cost (PKR) |
| ------------------------------------ | ----------------------------------------------------------------------------------------------- | -------------------- |
| **Mobile App (Android)**             | A basic Android app connected to the same backend (WebView or API-based)                        | 12,000 – 18,000 PKR  |
| **Mobile App (Android + iOS)**       | Cross-platform mobile app using React Native / Flutter with API integration                     | 40,000 – 60,000 PKR  |
| **Live Class Integration**           | Integration of Zoom/Google Meet scheduling and join links inside dashboard                      | 7,000 – 12,000 PKR   |
| **Discussion Forum / Q&A Section**   | Students can ask questions, comment, interact with mentors                                      | 12,000 – 18,000 PKR  |
| **Automatic Certificate Generation** | System auto-generates certificates after course completion with unique ID and verification page | 4,000 – 8,000 PKR    |
| **AI-Based Study Recommendations**   | System suggests study materials based on previous test results and activity                     | 25,000 – 40,000 PKR  |

---

## Recommended Combined Packages

| Package                            | Included Enhancements                                                   | Estimated Total Cost (PKR) |
| ---------------------------------- | ----------------------------------------------------------------------- | -------------------------- |
| **Professional Expansion Package** | Live Classes + Certificate Generator + Discussion Forum                 | 25,000 – 35,000 PKR        |
| **Mobile Learning Package**        | Android App + Live Classes + Certificate Generator                      | 32,000 – 45,000 PKR        |
| **AI Enhanced Platform Package**   | Android App + Discussion Forum + AI Study Recommendations + Certificate | 55,000 – 85,000 PKR        |

---

## Notes

1. Prices are **flexible based on complexity**, UI requirements, and hosting/server upgrades if needed.
2. All enhancements will integrate seamlessly with the existing system.
3. Development time varies per module; typically 1–4 weeks depending on scope.

---

### This document and the system design contained within are the intellectual property of the developer **Anon** and may not be reproduced, distributed, or used for implementation without prior written consent.
