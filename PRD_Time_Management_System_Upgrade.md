# Product Requirements Document (PRD)
## Time Management System Upgrade

| Field | Details |
|-------|---------|
| **Document Title** | Time Management System Upgrade - PRD |
| **Version** | 1.0 |
| **Date** | 2025 |
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
| FR-4.1.4 | Search Functionality | Implement search button/functionality as an alternative to scrolling (wishlist item) |
| FR-4.1.5 | User Hierarchy & Approval | All new projects/tasks must be approved by Head of Department (HoD), not system admin. Users can create items subject to HoD approval |
| FR-4.1.6 | Number Range Visibility | Enable view of all numbers (0xxx-9xxx) with appropriate access restrictions |
| FR-4.1.7 | Access Restrictions | Users without proper access cannot click or view details of restricted items |
| FR-4.1.8 | Public Holidays by Country | Include public holidays for respective countries. Users must be assigned to a country to view relevant holidays |

#### Cost Center Code Structure

| Code | Category | 1000-4000: Operational Tasks | x500: Meetings & Coordination |
|------|----------|------------------------------|-------------------------------|
| 0 | General & Corporate | 0100: Town Hall / General Assembly<br>0200: Health & Safety (HSE) Briefings<br>0300: Team Building / Company Events | 0500: General Corporate Updates<br>0510: Safety Committee Meetings |
| 1 | Proposal & Tendering | 1100: Solution Design & Layout<br>1200: Costing & BOM Estimation<br>1300: Tendering Documentation | 1500: Internal Tender Sync<br>1510: External Client Pitch / Presentation<br>1520: Site Walk/Survey Meeting |
| P | Project Execution | See Project Execution Breakdown below | (N/A) |
| 2 | Research & Dev | 2100: Internal Tooling Development<br>2200: Hardware/Sensor Testing<br>2300: R&D Documentation | 2500: R&D Brainstorming<br>2510: Technical Workshops<br>2520: Vendor Demo / Tech Presentation |
| 3 | PHs & Leaves | 3100: Annual Leave<br>3200: Medical / Sick Leave<br>3300: Public Holiday<br>3400: Compassionate/Special Leave | (N/A) |
| 4 | Internal Operation | 4100: Office Admin / Maintenance<br>4200: Finance & Bookkeeping<br>4300: Supply Chain & Logistics | 4500: Management Strategy Meeting<br>4510: Weekly Operations Sync<br>4520: Finance Audit Review |
| 5 | Business Dev | 5100: Lead Generation / Sales<br>5200: Marketing & Social Media<br>5300: Exhibition Planning | 5500: Sales Pipeline Review<br>5510: Marketing Strategy Meeting<br>5520: Networking / External Seminars |
| 6 | Technical Support | 6100: Warranty Services (Hands-on)<br>6200: Maintenance (Scheduled)<br>6300: Ad-hoc Repairs | 6500: Support Case Review<br>6510: Maintenance Planning Sync |
| 7 | IT & Infrastructure | 7100: Server & Network Admin<br>7200: Asset/Hardware Maintenance<br>7300: Internal Systems (TMS Fixes) | 7500: IT Security / VPN Sync<br>7510: TMS Technical Review Meeting |
| 8 | Project Control | 8100: Internal Auditing (TMS vs Bukku)<br>8200: Data Normalization / Cleaning<br>8300: Process Workflow Development | 8500: Audit Clarification Meeting<br>8510: PRD/Process Review<br>8520: Budget vs Actual Presentation |
| 9 | Human Resource | 9100: Payroll & Staff Claims<br>9200: Recruitment & Interviewing<br>9300: Training & Induction | 9500: Hiring & Strategy Meeting<br>9510: Staff Appraisal (1-on-1)<br>9520: Training / Onboarding Sync |

#### 1. System Architecture: The "Parent-Child" Logic

To maintain data integrity, the system shall utilize a two-tier selection process:

| Tier | Description | Example |
|------|-------------|---------|
| **Tier 1 (Parent)** | The Project ID | P1048, P1053 |
| **Tier 2 (Child)** | The Activity Code | 420 - On-site Installation |

#### 2. Project Execution (P-Series) Activity Codes

These codes apply to all project-based work (e.g., P1048, P1053).

| Phase | Activity Code | Task Name & Included Activities |
|-------|---------------|--------------------------------|
| **100: Initiation** | 101 | Kickoff Meeting & Project Charter |
| | 110 | Technical Proposal (Layout, AMR Qty, Proposal) |
| | 120 | VC Simulation (Map Editing, Process Flow, Modeling, Video) |
| | 130 | RCS Simulation (Map Configuration, RCS Video) |
| | 140 | Commercial & Legal (Offer, Contract, Tech Agreement) |
| **200: Planning** | 201 | Project Plan & Software Development Plan |
| | 210 | Supply Chain (BOM List, Procurement) |
| | 220 | Site Prep (Floor Inspection, Travel Preparation) |
| **300: SW Dev** | 301 | Planning, Feasibility & Requirement Gathering |
| | 310 | Design & Architecture (UI/UX, DB, Infra, Security) |
| | 320 | Implementation (Frontend, Backend, Integration, Env) |
| | 330 | Testing & QA (Unit, E2E, Performance, UAT) |
| | 340 | Deployment, Maintenance & Monitoring |
| **400: Execution** | 401 | In-house Pre-Comm & Internal Testing |
| | 410 | Factory Acceptance Test (FAT) & Deliveries |
| | 420 | On-site Install (QR/Rack, Robot Setup, Branding) |
| | 430 | Commissioning & Ramp-up Optimization |
| **500: Closing** | 501 | Customer Training & Handover Documentation |
| | 510 | Project Sign-off |
| | 520 | Tech Support (Remote, Onsite, Patch/Update) |

### 4.2 Notifications & Approval System (Priority: High)

**Requestor:** Eng Jing Hao (Product & Solution)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.2.1 | Task/Subtask Approval Notifications | Notify project admin when a new task/subtask requires approval |
| FR-4.2.2 | Email Prompts | Send email prompts for pending request approvals |
| FR-4.2.3 | Visual Indicators | Display icon/label on side tab for pending approvals |
| FR-4.2.4 | Project Dashboard | Display full project dashboard with summary view |
| FR-4.2.5 | Dashboard Filtering | Implement week-based filtering option (filter when needed, not default) |

### 4.3 Clock-In/Clock-Out Functionality (Priority: High)

**Requestor:** Lim Kai Xuan (Robotic Application - Frontend)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.3.1 | Date Navigation | Implement quick date selection via small dropdown calendar instead of week-by-week scrolling |
| FR-4.3.2 | Lunch Break Automation | Allow users to set default lunch time to avoid double clock-in (morning and afternoon sessions). Since lunch hours are consistent daily, system should auto-deduct lunch break |
| FR-4.3.3 | External Access | Make system accessible as an external website, not limited to internal network/VPN access. This is critical for on-site clock-in scenarios |

### 4.4 Task Management (Priority: Medium)

**Requestor:** Norazlynn (FA & HR)

| Req ID | Requirement | Description |
|--------|-------------|-------------|
| FR-4.4.1 | Streamlined Task Approval | Improve task creation approval process - consider limiting approval scope to specific topics/categories |
| FR-4.4.2 | Drag & Drop Rearrangement | Implement drag function to rearrange task order |
| FR-4.4.3 | Auto-Numbering | Auto-assign numbers to tasks to prevent duplicate numbering across different groups |
| FR-4.4.4 | Duplicate Number Resolution | Resolve existing duplicate numbers (e.g., 9993 appearing twice for different members in different groups) |

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
| **P4 - Low (Wishlist)** | Search functionality for dropdowns, Analog clock selector |

---

## 8. Success Metrics

| Metric | Target |
|--------|--------|
| Clock-in completion time | Reduce by 50% |
| Task approval turnaround | Reduce from days to hours |
| User satisfaction score | Increase to 4.0/5.0 |
| Duplicate task numbers | Reduce to 0 |
| On-site clock-in success rate | 100% (without VPN dependency) |
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

## 11. Timeline (Proposed)

| Phase | Duration | Deliverables |
|-------|----------|--------------|
| **Phase 1: Foundation** | Weeks 1-3 | Cost center standardization, External access setup, Security implementation |
| **Phase 2: Core Features** | Weeks 4-7 | Approval workflows, Notifications, Clock-in improvements, Dashboard |
| **Phase 3: Enhanced Features** | Weeks 8-10 | Templates, Duplication, Drag & drop, Reporting |
| **Phase 4: UI/UX Polish** | Weeks 11-12 | Interface improvements, Testing, Bug fixes |
| **Phase 5: Deployment** | Week 13 | Go-live, Training, Support |

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
