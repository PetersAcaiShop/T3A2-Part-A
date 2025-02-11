# Smoothie & Açaí Shop Online Ordering App

## Table of Contents

- [Smoothie \& Açaí Shop Online Ordering App](#smoothie--açaí-shop-online-ordering-app)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
    - [Tech Stack](#tech-stack)
  - [Dataflow Diagram](#dataflow-diagram)
  - [Application Architecture](#application-architecture)
    - [Presentation Layer](#presentation-layer)
    - [Business Logic Layer](#business-logic-layer)
    - [Data Access Layer](#data-access-layer)
  - [User Stories](#user-stories)
    - [Customer Perspective](#customer-perspective)
    - [Shop Owner Perspective](#shop-owner-perspective)
  - [Customer Flow](#customer-flow)
  - [Wireframes](#wireframes)
    - [Screenshots](#screenshots)
  - [Git Workflow Using Git Flow](#git-workflow-using-git-flow)
    - [Main Branches](#main-branches)
    - [Supporting Branches](#supporting-branches)
    - [Workflow](#workflow)
  - [Trello Board](#trello-board)
    - [Board Structure](#board-structure)

## Project Overview

The Smoothie & Açaí Shop Online Ordering App aims to enhance customer experience and streamline operations for a health-focused retail business. The app provides a user-friendly platform for customers to browse menus, customise orders, and track their orders, while offering efficient management tools for shop owners.

### Tech Stack

- **Front-end**: React.js
- **Back-end**: Node.js & Express
- **Database**: MongoDB
- **Design Tools**: Figma

## Dataflow Diagram

The Data Flow Diagram (DFD) visually represents how data moves through the application. It illustrates the interaction between users and the different layers of the system. Here's a detailed breakdown:

- **User Interaction Layer:** This is where users interact with the application via the front-end. When a user browses the menu, customizes an order, or makes a payment, these actions initiate data flow.
- **Data Input:** User actions are input to the system. For instance, when browsing the menu, the user is requesting data from the server.
- **Back-End Processing Layer:** The back-end, built with Node.js and Express, receives user requests. It processes these requests, interacts with the database, and sends responses back to the front-end. This layer handles business logic, such as calculating order totals and validating user inputs.
- **Data Storage:** The database, using MongoDB, stores all data related to the application. This includes menu items, user information, and order details. Data is read from and written to the database by the back-end.
- **Data Output:** The back-end sends processed data to the front-end. This might include displaying a menu, updating order status, or confirming a payment.
- **Data Flow:** The DFD also shows how the data flows between these layers. For example, when a customer places an order, the flow is: user input on the front-end, request to back-end, data processing and storage in the database, and confirmation back to the front-end. The specific details of this flow will be illustrated in the diagram itself.

[Insert DFD Here]

## Application Architecture

The Application Architecture Diagram (AAD) illustrates the different components of the application and how they interact. The application follows a layered architecture to ensure a separation of concerns and scalability. Here's a detailed explanation:

### Presentation Layer

This layer is the front-end of the application, built with React.js.
It handles user interface and user experience.
It is responsible for displaying information and receiving user inputs.

### Business Logic Layer

This layer is the back-end of the application, built using Node.js and Express.
It manages the core functionality of the application.
It handles data validation, processing, and interaction with the data access layer.

### Data Access Layer

- This layer manages how data is stored and retrieved from the database.
- It uses MongoDB to store the data with Mongoose as the Object Relational Mapper (ORM).
- It is responsible for handling database operations such as CRUD (Create, Read, Update, Delete).

[Insert Diagram Here]

## User Stories

Categorised by user roles, these stories highlight key functionalities.

### Customer Perspective

- As a customer, I want to browse the menu to explore available smoothies and açaí bowls.
- As a customer, I want to customise my order to include specific add-ons.
- As a customer, I want to track my order status to know when it's ready.

### Shop Owner Perspective

- As a shop owner, I want to manage menu items to update prices and descriptions.
- As a shop owner, I want to view sales reports to analyse revenue trends.

## Customer Flow

The sequence of actions taken by a customer to engage with the web application.

## Wireframes

Visual designs for key app screens ensure an intuitive user experience.

### Screenshots

1. **Menu Browsing**
2. **Order Customisation**
3. **Checkout Process**
4. **Order Tracking**

## Git Workflow Using Git Flow

The Git Flow workflow is used to manage source code, branching, and releases. Here's a description of the workflow:

### Main Branches

**main:** This branch contains the official release history.
**develop:** This is the main development branch from where all feature branches are branched from.

### Supporting Branches

**feature:** Feature branches are created for each new feature or task. They are branched from develop and merged back into develop after completion.
**release:** Release branches are created to prepare for a new release. They are branched from develop and merged into main and develop after release.
**hotfix:** Hotfix branches are created to fix bugs in production. They are branched from main and merged back into main and develop after the fix.

### Workflow

- New features are developed on feature branches branched from the develop branch.
- Once completed, feature branches are merged back into the develop branch.
- When ready for release, a release branch is created from the develop branch.
- After testing, the release branch is merged into the main branch, and also back into develop.
- If a bug is found in the main branch, it is addressed by creating a hotfix branch.
- After the bug is fixed, the hotfix branch is merged into main and also develop.

- **Version Control:** Git is used for version control, and all code changes are made using commits and pull requests.
- **Team Collaboration:** Git workflow provides a structured way for all team members to collaborate efficiently on the project.
- **Source Control:** This workflow ensures proper source control methodology and maintains a clean and organised project.
- **Branching Strategy:** Using a structured branching strategy like Git Flow helps manage code, facilitate collaboration, and ensure a stable and well maintained repository.

![GitFlow Diagram](./docs/git-flow.png)

## 📌 GitHub Projects Board: Kanban for Agile Project Management & Sprint Planning

To ensure efficient project tracking and agile preparation for Part B, we utilize a Kanban-style GitHub Projects board, central to visualizing workflow and managing tasks throughout the Merry Berry project.  We consistently adhere to **simple and clear Kanban standards**, evidenced in the dated screenshots below, which also illustrate our sprint planning for Part B development.

### Screenshots (Throughout Part A Documentation):**

#### Early Stage (Feb 9th)
![Early Stage](./docs/kanban/kanban_board_early_stage.png)

#### Mid Stage (Feb 11th)
![Mid Stage](./docs/kanban/kanban_board_mid_stage.png)

#### Late Stage (Feb 14th)
![Late Stage](./docs/kanban/kanban_board_late_stage.png)

These screenshots, alongside the following standards, demonstrate our organized Kanban approach and Part B sprint planning.

### 📋 Kanban Board Standards: Clear, Simple, and Consistently Applied

Our GitHub Projects board adheres to these key standards:

#### ✔️ Consistent Card Naming:  `[Feature Area] - [Concise Task Description]`

Uniform card naming using `[Feature Area] - [Concise Task Description]` (e.g., `[README] - HD Polish & Proofread`) ensures immediate task identification and categorization, as shown in the **"Issues List View" screenshot**.

#### ✔️ Meaningful Label Usage:  Categorization, Priority, Workload

Diverse labels categorize tasks for clarity:

*   **Documentation Type:** `Wireframes`, `User Stories`, `AAD`, `DFD`, `Kanban`, `README` (visually categorized in **"Issues List View" screenshot**).
*   **Priority:** `Urgent` (`P0`), `High` (`P1`), `Medium` (`P2`) (priority labels in **"Kanban Board Overview" screenshots**).
*   **Size Estimate:** `XS`, `S`, `M`, `L`, `XL` (for workload awareness).

**The "Issues List View" screenshot effectively showcases this varied and meaningful label application.**

#### ✔️ Clear Assignee Usage:  Accountability

Each task is assigned to a team member for accountability, clearly visible by avatars in **"Kanban Board Overview" screenshots** within "In progress" and "In review" columns.

#### ✔️ Well-Defined Kanban Workflow:  Progress Tracking

Workflow columns track task status:

*   **Backlog:** Prioritized tasks (P0-P2 labels), ready for "Ready".
*   **Ready: Requirements Clear & Capacity Available:** Queue for "In progress".
*   **In progress:** Tasks actively being worked on.
*   **In review: Awaiting Quality Assurance Review.**
*   **Done:** Completed, reviewed tasks.

**"Kanban Board Overview" screenshots demonstrate tasks moving through these workflow stages throughout Part A.** Column descriptions on our live board further clarify each stage (e.g., "Ready: Requirements Clear & Capacity Available").

#### ✔️ Granular Checklists:  Subtask Management

Checklists within Issue cards break down complex tasks into sub-steps, exemplified in the **"Example Issue Detail" screenshot**.

### 🗓️ Sprint Planning for Part B:  Kanban-Informed Development Sprints

Extending Kanban, we planned Part B sprints around client/server milestones.  Sprints are timeboxed (e.g., 1-week), iterative, and goal-focused.  **Example: Backend Sprint 1 (Core API & Database Setup):**

*   **Goal:**  Establish foundational backend.
*   **Tasks (from Kanban Backlog):**
    *   `[Backend] - Set up Backend Project & MongoDB Database` ([Team Member])
    *   `[Backend] - Implement User Model & Auth API` ([Team Member])
    *   `[Database] - Design MongoDB Schemas (User, Menu)` ([Team Member])

Sprint backlogs are created by selecting prioritized tasks from Kanban "Backlog," utilizing priority and size labels for delegation.

### 🚀 Reflection:  HD Project Management - Kanban Throughout & Sprint-Ready

Our Kanban board, evidenced by dated screenshots, demonstrates consistently applied, simple and clear standards for HD project management throughout Part A and informs our sprint-based approach for Part B.  This agile methodology ensures transparency, accountability, and organized progress from documentation to development.

#### Kanban Board Overview
![Kanban Board Overview](./docs/kanban/kanban_board_overview.png)

#### Issues List View
![Issues List View - Showing Card Names and Labels](./docs/kanban/kanban_board_issues_list_hd_labels.png)

#### Example Issue Detail
![Example Issue Detail](./docs/kanban/kanban_example_issue.png)