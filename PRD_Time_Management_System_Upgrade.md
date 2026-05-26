# Product Requirements Document (PRD)
## Time Management System Upgrade

| Field | Details |
|-------|---------|
| **Document Title** | Time Management System Upgrade - PRD |
| **Version** | 2.0 |
| **Date** | 2026 |
| **Status** | Draft |
| **Author** | Project Controller |
| **Stakeholders** | Internal Operations, Product & Solution, Robotic Application, FA & HR, Robotic DevOps |

---

## 1. Executive Summary

This PRD outlines the requirements for upgrading the company's Time Management System based on comprehensive feedback gathered from team members across multiple departments. The upgrade aims to improve user experience, streamline workflows, enhance approval processes, and provide better reporting and dashboard capabilities.

---

## 2. Problem Statement

The current Time Management System has several pain points identified by team members:

- Inconsistent cost center/department numbering and classification
- Limited navigation and date selection capabilities in the clock-in interface
- Lack of external network access for on-site clock-in
- Inefficient approval workflows and notification systems
- Missing dashboard and reporting features
- UI/UX inconsistencies and usability issues
- No project templates or duplication capabilities
- Manual task numbering leading to duplicates

---

## 3. Objectives

1. Standardize cost center and department classification across the organization
2. Improve user experience with better navigation, calendars, and UI elements
3. Implement robust approval workflows with proper notifications
4. Enhance dashboard and reporting capabilities
5. Enable external access for on-site time tracking
6. Provide project templates and duplication features
7. Automate task numbering to prevent duplicates

---

## 4. Functional Requirements

### 4.1 Cost Center & Department Classification (Priority: High)

**Requestor:** Racheal Choo (Internal Operation)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.1.1 | Standardized Cost Center Assignment | Implement a structured numbering system (0-9, P) for departments/categories with operational tasks (1000-4000) and meetings/coordination (x500). See detailed breakdown below. |
| FR-4.1.2 | Cost Center List Management | Collaborate with stakeholders to create a definitive, non-random list of cost centers for each department |
| FR-4.1.3 | Dropdown Navigation | Replace scrolling lists with dropdown menus on each header for easier navigation |
| FR-4.1.4 | User Hierarchy & Approval | All new projects/tasks must be approved by Head of Department (HoD), not system admin. Users can create items subject to HoD approval |
| FR-4.1.5 | Number Range Visibility | Enable view of all numbers (0xxx-9xxx) with appropriate access restrictions |
| FR-4.1.6 | Access Restrictions | Users without proper access cannot click or view details of restricted items |
| FR-4.1.7 | Public Holidays by Country | Include public holidays for respective countries. Users must be assigned to a country to view relevant holidays |

#### Cost Center Code Structure

| Dept # | Department Name | Block | Code | Activity Name | Description / Placement |
|--------|-----------------|-------|------|---------------|-------------------------|
| 1 | Sales & Project | 81xx | 8110 | Tendering & Props | Tech Proposal, Layout & Quotes |
| | | | 8120 | Business Dev | Lead Gen & Client Pitching |
| | | | 8190 | Sales Meetings | External Client Syncs |
| 2 | Application | 82xx | 8210 | Backend Dev | API, Logic, DB & DevOps |
| | | | 8220 | Frontend Dev | UI/UX, HMI & Integration |
| | | | 8230 | System QA | Testing, Bug Fixing & QA |
| | | | 8290 | App Meetings | Technical Syncs & Sprint Planning |
| 3 | Product & Solution | 83xx | 8310 | Simulations | VC/RCS Modeling |
| | | | 8320 | Solution Design | High-Level Architecture & R&D |
| | | | 8390 | R&D Meetings | Internal Design Reviews |
| 4 | Internal Operation | 91xx | 9111 | HR Admin | Payroll, Claims & Benefits |
| | | | 9112 | Recruitment | Hiring & Onboarding |
| | | | 9121 | Accounting (DR) | Daily Routine: Accounting |
| | | | 9122 | FYE (DR) | Daily Routine: Year End |
| | | | 9123 | Accounting (RR) | Review/Reporting: Accounting |
| | | | 9124 | FYE (RR) | Review/Reporting: Year End |
| | | | 9125 | Projections | Monthly Budget & Cashflow |
| | | | 9131 | Shipment | Planning & Documentation |
| | | | 9141 | Gov Paperwork | Official Paperwork & Gov Topics |
| | | | 9142 | Official Visits | Gov offices, Seminars, Offline |
| | | | 9143 | Miscellaneous | General Admin Tasks |
| | | | 9151 | Project Control | Auditing & Normalization |
| | | | 9152 | Process Dev | SOPs, PRD & Gap Analysis |
| | | | 9153 | Tools Dev | Learning/Explore new tools |
| | | | 9190 | Meeting | Internal Ops Syncs |
| 5 | General | 98xx | 9810 | Corporate | Town Halls, HSE & Events |
| | | | 9820 | Onboarding | System Exploration (New Joiners) |
| | | | 9830 | Super Summary | Weekly Reporting tasks |
| | | | 9890 | Management Meeting | Weekly Ops & Management Strategy |
| 6 | Leaves & Absence | 99xx | 9910 | Annual Leave | Approved Personal Leave |
| | | | 9920 | Medical Leave | MC / Sick Leave |
| | | | 9930 | Public Holiday | Gazetted Holidays |
| | | | 9940 | Unpaid Leave | Leave without pay |

#### 1. System Architecture: The "Parent-Child" Logic

To maintain data integrity, the system shall utilize a two-tier selection process:

| Tier | Description | Example |
|------|-------------|---------|
| **Tier 1 (Parent)** | The Project ID | P1048, P1053 |
| **Tier 2 (Child)** | The Activity Code | 440 - On-site Installation |

#### 2. Project Execution (P-Series) Activity Codes

These codes apply to all project-based work (e.g., P1048, P1053).

| Phase | Activity Code | Task Name & Included Activities |
|-------|---------------|--------------------------------|
| **100: Initiation** | 110 | Kickoff Meeting & Project Charter |
| | 120 | Technical Proposal (Layout, AMR Qty, Proposal) |
| | 130 | VC Simulation (Map Editing, Process Flow, Modeling, Video) |
| | 140 | RCS Simulation (Map Configuration, RCS Video) |
| | 150 | Commercial & Legal (Offer, Contract, Tech Agreement) |
| **200: Planning** | 210 | Project Plan & Software Development Plan |
| | 220 | Supply Chain (BOM List, Procurement) |
| | 230 | Site Prep (Floor Inspection, Travel Preparation) |
| **300: SW Dev** | 310 | Planning, Feasibility & Requirement Gathering |
| | 320 | Design & Architecture (UI/UX, DB, Infra, Security) |
| | 330 | Implementation (Frontend, Backend, Integration, Env) |
| | 340 | Testing & QA (Unit, E2E, Performance, UAT) |
| | 350 | Deployment, Maintenance & Monitoring |
| **400: Execution** | 410 | In-house Pre-Comm & Internal Testing |
| | 420 | Factory Acceptance Test (FAT) & Deliveries |
| | 430 | System Management |
| | 440 | On-site Install (QR/Rack, Robot Setup, Branding) |
| | 450 | Commissioning & Ramp-up Optimization |
| **500: Closing** | 510 | Customer Training & Handover Documentation |
| | 520 | Project Sign-off |
| | 530 | Tech Support (Remote, Onsite, Patch/Update) |

### 4.2 Notifications & Approval System (Priority: High)

**Requestor:** Eng Jing Hao (Product & Solution)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.2.1 | Task/Subtask Approval Notifications | Notify project admin when a new task/subtask requires approval |
| FR-4.2.2 | Microsoft Teams Notifications | Notifications will be sent via Microsoft Teams chat instead of email. |
| FR-4.2.3 | Visual Indicators | Display icon/label on side tab for pending approvals |
| FR-4.2.4 | Project Dashboard | Display full project dashboard with summary view |
| FR-4.2.5 | Dashboard Filtering | Implement week-based filtering option (filter when needed, not default) |

### 4.3 Clock-In/Clock-Out Functionality (Priority: High)

**Requestor:** Lim Kai Xuan (Robotic Application - Frontend)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.3.1 | Date Navigation | Implement quick date selection via small dropdown calendar instead of week-by-week scrolling |
| FR-4.3.2 | Lunch Break Automation | Allow users to set default lunch time to avoid double clock-in (morning and afternoon sessions). Since lunch hours are consistent daily, system should auto-deduct lunch break |

### 4.4 Task Management (Priority: Medium)

**Requestor:** Norazlynn (FA & HR)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.4.1 | Streamlined Task Approval | Improve task creation approval process - consider limiting approval scope to specific topics/categories |
| FR-4.4.2 | Drag & Drop Rearrangement | Implement drag function to rearrange task order |
| FR-4.4.3 | Duplicate Number Resolution | Resolve existing duplicate numbers (e.g., 9993 appearing twice for different members in different groups) |

### 4.5 UI/UX Improvements (Priority: Medium)

**Requestor:** Pong Wei Xiang (Robotic DevOps - Backend)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.5.1 | Edit Button Placement | Relocate edit button for projects - move from top to a more accessible location near the project search/list area |

### 4.6 Dashboard & Reporting (Priority: High)

**Requestor:** Jade (Internal Operation)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.6.1 | Project Summary View | When selecting a project, directly display start week and end week |
| FR-4.6.2 | Hours Summary Dashboard | Display summary of total hours for each activity/person vs. budget |
| FR-4.6.3 | Project Duplication | Implement duplicate function to directly duplicate from existing project |
| FR-4.6.4 | Weekly Data Extraction | Enable data extraction based on project weekly |
| FR-4.6.5 | Activity Rearrangement | Implement drag function to rearrange order of activities |
| FR-4.6.6 | Project Templates | Create templates for all projects (currently projects are clocked in freely without structure) |
| FR-4.6.7 | Homepage Create Project | Add "Create Project" icon to homepage |
| FR-4.6.8 | Member Management | Enable adding members during project creation |

### 4.7 Time Entry Interface (Priority: Medium)

**Requestor:** Brendon (Product & Solution)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.7.1 | Right-Click Edit | Add right-click edit function for users who have expanded sections |
| FR-4.7.2 | End Time & Auto-Calculation | Add "End Time" field; system auto-calculates time spent and records in "Spent Hours" section |
| FR-4.7.3 | Auto-Populate Project Details | Project details should auto-update when users select options (e.g., "Layout") - users only need to input date/time |
| FR-4.7.4 | Calendar Dropdown | Implement calendar dropdown for date section |
| FR-4.7.5 | Time Selector | Add analog clock time selector for start time |
| FR-4.7.6 | Collapsible Sections | Minimize project details by default with expandable option |
| FR-4.7.7 | UI Alignment & Sizing | Improve alignment and increase webpage size to 125% of original for better readability |

---

## 5. Non-Functional Requirements

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| NFR-5.1 | Accessibility | System must be accessible externally (outside internal network/VPN) |
| NFR-5.2 | Performance | Dashboard and reporting features should load within 3 seconds |
| NFR-5.3 | Usability | UI should be intuitive with minimal training required |
| NFR-5.4 | Security | Role-based access control with proper authentication for external access |
| NFR-5.5 | Compatibility | Support modern web browsers (Chrome, Firefox, Edge, Safari) |
| NFR-5.6 | Responsiveness | Interface should be responsive and usable on various screen sizes |

---

## 6. User Roles & Permissions

| Role | Permissions |
|------|-------------|
| **System Admin** | Full system configuration, user management |
| **Head of Department (HoD)** | Approve projects/tasks, view department data, manage team |
| **Project Admin** | Manage projects, approve subtasks, view project dashboard |
| **Project Member** | Create tasks (subject to approval), clock-in/out, view own data |
| **Finance/HR** | View financial summaries, extract reports, manage cost centers |

---

## 7. Priority Matrix

| Priority | Features |
|----------|----------|
| **P1 - Critical** | External access for clock-in, Cost center standardization, Approval workflow with notifications, Dashboard with hours vs. budget |
| **P2 - High** | Date navigation improvements, Lunch break automation, Project templates, Auto-numbering |
| **P3 - Medium** | Drag & drop functionality, Right-click edit, UI alignment improvements, Weekly data extraction |
| **P4 - Low (Wishlist)** | Analog clock selector |

---

## 8. Success Metrics

| Metric | Target |
|--------|--------|
| Clock-in completion time | Reduce by 50% |
| Task approval turnaround | Reduce from days to hours |
| User satisfaction score | Increase to 4.0/5.0 |
| Duplicate task numbers | Reduce to 0 |
| On-site clock-in success rate | 100% |
| Dashboard load time | Under 3 seconds |

---

## 9. Dependencies & Assumptions

### Dependencies
- IT team to configure external access and security protocols
- HR to provide complete list of public holidays by country
- Department heads to finalize cost center numbering scheme
- Network team to enable external website hosting

### Assumptions
- All team members have access to modern web browsers
- Lunch break duration is consistent across the organization
- VPN access will be replaced or supplemented with secure external access
- Existing data will be migrated without loss

---

## 10. Risks & Mitigations

| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| External access security breach | High | Medium | Implement multi-factor authentication, SSL, and security audits |
| Resistance to new approval workflow | Medium | Medium | Provide training and clear documentation |
| Data migration issues | High | Low | Conduct thorough testing and maintain backups |
| Cost center numbering conflicts | Medium | High | Establish clear governance and single source of truth |
| Performance degradation with new features | Medium | Medium | Conduct load testing before deployment |

---

## 11. Timeline 

| Phase | Deadline | Deliverables |
|-------|----------|--------------|
| **Phase 1** | **2 June 2026** | Database migration and backend refactoring |
| | | FR-4.3.1: Date selection navigation |
| | | FR-4.4.2 & FR-4.6.5: Drag & drop sort |
| | | FR-4.5.1 & FR-4.7.1: Edit button placement |
| | | FR-4.6.3: Project duplication |
| | | FR-4.6.7: Add project in homepage |
| | | FR-4.7.2: Use end time for clock in |
| | | FR-4.7.6: Default collapse activity summary |
| | | FR-4.7.7: Sizing (preferred font size) |
| | | FR-4.1.1, FR-4.1.2, FR-4.1.3: Cost center |
| | | FR-4.2.3: Visual indicator for approval |
| | | FR-4.2.4: Set default date for project summary |
| | | FR-4.2.5 & FR-4.6.1: Weekly view for project summary |
| | | FR-4.3.2: Lunch break automation |
| | | **Fixes:** |
| | | FR-4.6.8: Add member to project |
| | | FR-4.7.3: Project details |
| | | FR-4.7.4 & FR-4.7.5: Calendar and clock dropdown |
| **Phase 2** | **23 June 2026** | FR-4.6.4: Weekly data extraction |
| | | FR-4.1.7: Public holidays by country |
| | | FR-4.2.2: Microsoft Teams notification |
| | | FR-4.6.2: Hours summary dashboard |
| | | FR-4.6.6: Project templates |

---

## 12. Appendix

### A. Feedback Sources

| Name | Department | Key Contributions |
|------|------------|-------------------|
| Racheal Choo | Internal Operation | Cost center classification, user hierarchy, access control |
| Eng Jing Hao | Product & Solution | Notifications, approval system, dashboard |
| Lim Kai Xuan | Robotic Application (Frontend) | Clock-in UX, external access, lunch automation |
| Norazlynn | FA & HR | Task approval, drag & drop, auto-numbering |
| Pong Wei Xiang | Robotic DevOps (Backend) | UI placement improvements |
| Jade | Internal Operation | Dashboard, templates, reporting, duplication |
| Brendon | Product & Solution | Time entry UI, auto-calculation, interface design |

### B. Glossary

| Term | Definition |
|------|------------|
| HoD | Head of Department |
| PRD | Product Requirements Document |
| VPN | Virtual Private Network |
| UI/UX | User Interface / User Experience |
| FA & HR | Finance & Administration and Human Resources |
| TMS | Time Management System |
| HSE | Health, Safety & Environment |
| BOM | Bill of Materials |
| AMR | Autonomous Mobile Robot |
| VC | Visual Components |
| RCS | Robot Control System |
| FAT | Factory Acceptance Test |
| UAT | User Acceptance Testing |

---

*End of Document*
