#  Bride Assistant App

> A comprehensive Android application designed to simplify and centralize wedding planning for brides in Saudi Arabia's Eastern Province — combining budgeting, vendor discovery, task management, guest coordination, and cultural context into one intuitive platform.

<br>
----
<img width="1430" height="845" alt="brides_assistant_screens png" src="https://github.com/user-attachments/assets/1cb230c0-58e1-41b7-81ac-dc331ea3151c" />


----

**Senior Project  — Bachelor of Science in Information Technology**  
College of Computing & Informatics (CCI), Saudi Electronic University




---

##  Table of Contents

- [About the Project](#-about-the-project)
- [Problem Statement](#-problem-statement)
- [Features](#-features)
- [System Architecture & Design](#-system-architecture--design)
- [Tech Stack](#-tech-stack)
- [Methodology](#-methodology)
- [Testing & Evaluation](#-testing--evaluation)
- [Research Background](#-research-background)
- [Challenges & Learnings](#-challenges--learnings)
- [Future Work](#-future-work)

---

##  About the Project

Wedding planning in Saudi Arabia's Eastern Province is a deeply cultural, logistically complex, and emotionally demanding process. Brides are expected to coordinate vendors, manage tight budgets, maintain large guest lists, and navigate strong cultural traditions — all at the same time.

Existing apps fail to address this gap in two critical ways: they lack local vendor integration specific to the Eastern Province, and they don't account for the cultural nuances that shape Saudi weddings. Brides are left stitching together spreadsheets, informal notes, and scattered digital tools.

The **Bride Assistant App** was built to fix that. It is a single, culturally-aware Android platform that consolidates all wedding planning needs, reduces stress, and empowers brides to manage their big day with clarity and confidence.

---

##  Problem Statement

Traditional wedding planning methods in the Eastern Province suffer from:

- **No local focus** — most existing apps don't surface Saudi vendors or respect regional customs
- **Fragmented tools** — brides juggle spreadsheets, messaging apps, and paper checklists with no unified system
- **No budget visibility** — tracking expenses manually across multiple vendors leads to overspending
- **Task overload** — with no centralized task management, critical planning steps get missed
- **Emotional burden** — the pressure of cultural expectations and family coordination intensifies the stress of manual planning

---

##  Features

###  User Authentication & Account Management
Users can register an account by providing their full name, email, password, address, and phone number. The system supports secure login via email/password credentials and includes a password recovery flow via email reset link. A separate admin panel allows platform administrators to manage users, stores, and categories independently from the bride-facing interface.

###  Budget Management
Brides can define a total wedding budget and log individual expenses against it. The system tracks spending in real time, generates visual budget reports, and triggers alerts when spending approaches the set limit. The budget screen was updated during development based on user testing feedback to include an expense tracking summary box for clearer financial visibility.

###  Vendor Directory
The app provides a curated directory of local vendors and stores in the Eastern Province, organized by category (e.g., photography, catering, décor, entertainment). Users can browse vendor profiles, read reviews and ratings, and contact vendors directly through the app. Admins manage the vendor database — they can add, update, block vendors, and manage categories — ensuring the directory stays accurate and relevant.

###  Task Organization
Brides can create a personalized wedding checklist, assign deadlines to individual tasks, and track completion progress. Tasks are saved persistently and displayed in an organized list, allowing brides to stay on top of all planning steps — from sending invitations to signing vendor contracts.

###  Guest List Management
The app includes a full guest list module where brides can add guests by name and relationship, track RSVP statuses, and manage the overall headcount. The guest list is saved and updated in real time, eliminating the need for manual spreadsheets.

###  Wedding Information & Countdown
Brides enter their wedding date and venue in a dedicated screen. The app automatically calculates and displays a live countdown to the wedding day, updating dynamically as the date changes. This feature was refined during development based on supervisor feedback to include the countdown box as a prominent UI element.

###  Ratings & Comments
Users can leave ratings and comments on vendor profiles, contributing to a community-driven quality signal for other brides searching the directory.

###  Admin Panel
A dedicated admin interface handles platform management separately from the bride's experience. Admins can: view and manage the full users list, add or update vendor/store listings, block vendors who violate platform policies, and manage store categories.

---

##  System Architecture & Design

The system was designed using a full set of standard UML and architectural diagrams:

| Diagram | Purpose |
|---|---|
| **Use Case Diagram** | Captures all user and admin interactions with the system |
| **Entity Relationship Diagram (ERD)** | Models the database structure and relationships between entities |
| **Class Diagram** | Defines the complete object model of the application |
| **Sequence Diagram** | Illustrates the flow of interactions between system components over time |
| **Component Diagram** | Shows how the application's modules are organized and connected |
| **Deployment Diagram** | Describes the physical deployment of components across environments |

The architecture separates concerns between the Android front-end (built in Android Studio / Java), the Firebase real-time backend (authentication + database), and the admin panel — each with its own interaction model and access rights.

---

##  Tech Stack

| Layer | Tool |
|---|---|
| **IDE** | Android Studio |
| **Language** | Java |
| **Backend & Database** | Firebase (Real-time Database, Authentication, Cloud Messaging) |
| **Emulator** | BlueStacks App Player |

**Firebase** was selected as the backend for its real-time data synchronization, built-in authentication services, and its ability to handle large volumes of data efficiently — all well-suited to the app's multi-user, multi-module requirements.

---

##  Methodology

The project followed the **Waterfall software development methodology**, selected for three key reasons:

1. **Structured progression** — requirements were well-defined and stable from the outset, making Waterfall's sequential phases (requirements → design → implementation → testing → deployment) a natural fit
2. **Clear deliverables per phase** — each stage had specific outputs, simplifying progress tracking and timeline management
3. **Reduced rework risk** — with stable requirements, the risk of iterative scope changes was low, making the linear model more efficient than Agile for this project

---

##  Testing & Evaluation

The application was evaluated through structured black-box test cases covering all core user flows. Each test case specifies: identifier, priority, related use case, pre-conditions, input data, step-by-step execution, expected result, and post-conditions.

### Test Cases Summary

| # | Test Case | Priority | Key Inputs | Expected Outcome |
|---|---|---|---|---|
| TC-01 | User Create Account | High | Full name, email, password, address, phone | Account created; user redirected to confirmation page |
| TC-02 | User Login | High | Email, password | User authenticated; redirected to dashboard |
| TC-03 | Budget Management | High | Budget amount, expense details | Budget updated; running totals displayed correctly |
| TC-04 | Vendor Directory Access | High | Search criteria / category | Matching vendor list displayed; vendors contactable |
| TC-05 | Task Organization | High | Task details, deadline | Task added to checklist; saved and tracked |
| TC-06 | Guest List Management | High | Guest name, relationship | Guest list updated; entries persisted correctly |
| TC-07 | Add Wedding Information | High | Wedding date, wedding place | Date and place saved; countdown auto-updated |
| TC-08 | Admin Manage Vendor Store | High | Vendor update/block; category add/delete | Vendor details updated or blocked; categories managed |
| TC-09 | Forgot Password | High | Email address | Reset link sent; success message displayed |
| TC-10 | User Logout | High | Logout action | Session terminated; user redirected to login |
| TC-11 | Add Comments & Rating | High | Rating value, comment text | Rating and comment saved; visible on vendor profile |

All test cases were assigned **High** priority, reflecting their coverage of the app's core functional requirements.

---

##  Research Background

The project was grounded in a review of 14 studies spanning wedding planning systems, mobile application design, software development methodologies, Firebase architecture, and Saudi cultural context. Key findings that shaped the design:

- **Saudi wedding culture** — Eastern Province weddings involve multi-stage traditions (proposals, dowry negotiations, family coordination) that require a culturally sensitive digital tool. Generic international apps are insufficient for this context.
- **UI/UX in mobile apps** *(Durgekar et al., 2024)* — many apps fail user retention due to poor interface design. The project prioritized intuitive navigation and culturally appropriate visuals from the start.
- **Firebase for mobile backends** *(Chougale et al., 2021)* — Firebase's real-time database, authentication, and cloud messaging services were validated in the literature as well-suited to multi-user apps requiring data synchronization.
- **Recommender systems for event planning** — research on hybrid recommendation frameworks (content-based + collaborative filtering) informed the vendor directory design and provided a roadmap for AI-powered recommendations in future versions.
- **Security in Java development** *(Vyas, 2023)* — the project applied secure coding practices, dependency auditing, and robust authentication patterns to address common Java vulnerabilities including SQL injection and XSS.
- **Waterfall vs. Agile** *(Senarath & Rajarata, 2021)* — the comparative analysis of development methodologies confirmed Waterfall as the appropriate choice given the project's stable, well-scoped requirements.

---

##  Challenges & Learnings

**Building for a culturally specific audience**  
Designing for brides in the Eastern Province required more than feature parity with existing apps — it required understanding the role of family, tradition, and regional vendor ecosystems in Saudi weddings. The team had to make deliberate design decisions to ensure cultural appropriateness was built into the UX, not added as an afterthought.

**Real-time data consistency with Firebase**  
Managing real-time synchronization across multiple modules (budget, guests, vendors, tasks) simultaneously required careful structuring of the Firebase database schema to avoid race conditions and data conflicts.

**Iterative UI refinement based on feedback**  
Several screens were reworked mid-development based on supervisor feedback and user testing. The budget screen was updated to include a visual expense tracking summary, the wedding information screen was updated to include a prominent countdown display, and the Gantt chart was expanded to reflect additional chapters. This reinforced the importance of building with feedback loops even within a Waterfall framework.

**Admin vs. user separation**  
Maintaining a clean separation between the admin panel and the bride-facing interface — with different access controls, data views, and interaction models — required careful architecture planning, particularly around Firebase authentication rules and role-based access.

**Scope management in a team of five**  
Coordinating across five contributors with overlapping deliverables required explicit version tracking and clear ownership per feature. The revision history reflects the coordination overhead involved in delivering a production-grade report and application simultaneously.

---

##  Future Work

- **AI-powered vendor recommendations** — personalized suggestions based on the user's preferences, budget, and browsing behavior
- **Augmented reality venue previews** — let brides visualize décor and venue layouts before committing
- **Expanded vendor coverage** — extend the directory beyond the Eastern Province to cover more Saudi cities and regions
- **Multi-language support** — Arabic-first interface with additional language options for accessibility
- **In-app vendor booking & deals** — direct partnerships with local businesses to enable booking and exclusive offers from within the app

---

##  Academic Context

This project was submitted in partial fulfillment of the requirements for the **Bachelor of Science in Information Technology** at Saudi Electronic University, College of Computing & Informatics.

> Supervised by Dr. Huda Dakheel Allah Aljohani

---

*Built by five IT students from the Eastern Province — for brides from the Eastern Province. Where tradition meets technology.* 
