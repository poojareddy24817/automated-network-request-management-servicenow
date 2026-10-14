# Automated Network Request Management System in ServiceNow

**Candidate Name:** Pooja Reddy  
**Department / Degree:** B.Tech – Computer Science and Engineering  
**Institution:** Vignan Institute of Technology and Science  
**Academic Year:** 2026–2027  
**Platform:** ServiceNow Personal Developer Instance (`dev251577.service-now.com`)  
**Google Drive Project Folder:** [Google Drive Deliverables & Templates Folder](https://drive.google.com/drive/folders/1Y_ZW1ST9NaYQLa1UOgr6VpaGFqsu-t4n)  
**Demo Video:** [Watch Google Drive Demonstration](https://drive.google.com/file/d/1BnriywWde1DKvn6q077Kuw0jLV53ShrK/view?usp=drivesdk)  
**Submission Package:** `Automated_Network_Request_Management_Pooja_Reddy_Submission.zip`

---

## 📌 Project Overview
The **Automated Network Request Management System** is an end-to-end IT service management solution developed on ServiceNow. The system modernizes enterprise network provisioning by replacing manual, email-based requests with a standardized Service Catalog intake, automated Flow Designer orchestration, custom table database persistence, dynamic manager approvals, automated email notifications, and fulfillment task dispatch for network engineers.

---

## 🚀 Key Features & Architectural Capabilities
1. **Standardized Service Catalog Intake:**
   - Catalog Item: `Network Request1`
   - Variables (7): `Requested For`, `Mobile Number`, `Type of Connection` (Broadband, Fiber, Wireless), `Enter your existing id`, `Total Amount`, `Mode of Payment` (UPI, Card), and `Customer Address`.
   - Variable Set: `Requester information1`
   - Catalog UI Policy: `visible/hide of ID field` (dynamically renders and requires `Existing ID` when connection type is set to `Existing`).

2. **Zero-Code Workflow Orchestration (Workflow Studio / Flow Designer):**
   - Trigger: Service Catalog submission.
   - Core Action 1: `Get Catalog Variables` (extracts inputs into runtime execution data pills in 36 ms).
   - Core Action 2: `Create Record` (persists structured data into custom table `Database Table1` in 18 ms).
   - Core Action 3: `Send Email` (issues automated confirmation email to requester in 46 ms).
   - Core Action 4: `Ask for Approval` (routes approval to designated IT Manager / System Administrator).
   - Flow Branching Logic: `If Request is approved` -> `Update Record` (sets state to `Approved` and assigns to `ITIL User`) -> `Create Catalog Task` (`sc_task`).

3. **Custom Table Data Modeling & Persistence:**
   - Custom Table: `Database Table1` (`u_database_table1`)
   - Auto-generated identifier: `Database Number`
   - Dedicated fields: `u_requested_for`, `u_mobile_number`, `u_type_of_connection`, `u_total_amount`, `u_mode_of_payment`, `u_customer_address`, `u_approval_status`, `u_assignment_to`.
   - System Relationship: `Approval request1` on `sys_relationship` dynamically links approval records (`sysapproval_approver`) with custom table rows.

4. **Automated Notification Subsystem (`sys_email`):**
   - Generates responsive HTML notifications for:
     - Request creation: `Request REQ0010005 was created`
     - Managerial authorization: `Request REQ0010005 was approved`

5. **ITIL Task Fulfillment & Auditability:**
   - Automatically generates Catalog Tasks (`sc_task`) in the network engineering queue.
   - Complete audit trail across `sc_request` (REQ), `sc_req_item` (RITM), and `u_database_table1`.

---

## 📂 Project Templates & Phase Deliverables
All deliverables have been prepared in exact accordance with the official SmartBridge / SmartInternz project templates. Both editable Word documents (`.docx`) and high-fidelity PDF documents (`.pdf`) are available in the repository:

### 1. Ideation Phase (`Project_Deliverables/1. Ideation Phase/`)
- `Brainstorming- Idea Generation- Prioritization Template` (`.docx` / `.pdf`): Problem definition, idea listing into 4 thematic clusters, and 2x2 Impact vs. Effort prioritization matrix.
- `Define Problem Statements Template` (`.docx` / `.pdf`): Structured customer problem statement canvas for Requester, Approver, and Network Engineer.
- `Empathy Map Canvas` (`.docx` / `.pdf`): Persona analysis (Abraham Lincoln) detailing what the user thinks, feels, says, does, hears, pains, and gains.

### 2. Requirement Analysis (`Project_Deliverables/2. Requirement Analysis/`)
- `Customer Journey Map` (`.docx` / `.pdf`): 5-stage lifecycle from need identification to fulfillment, tracking touchpoints and emotional states.
- `Data Flow Diagrams and User Stories` (`.docx` / `.pdf`): DFD Level 0 (Context Diagram), DFD Level 1 (Decomposition Diagram), and complete User Stories (USN-1 to USN-10).
- `Solution Requirements` (`.docx` / `.pdf`): Functional requirements (FR-1 to FR-8) and Non-functional specifications (NFR-1 to NFR-6).
- `Technology Stack - Template` (`.docx` / `.pdf`): Multi-tier cloud architecture diagram, component descriptions (Table 1), and application characteristics (Table 2).

### 3. Project Design Phase (`Project_Deliverables/3. Project Design Phase/`)
- `Problem - Solution Fit Template v1` (`.docx` / `.pdf`): Problem-Solution Fit Canvas mapping customer problems to ServiceNow solutions.
- `Proposed Solution Template` (`.docx` / `.pdf`): Problem statement, novelty/uniqueness, target beneficiaries, and KPIs.
- `Solution Architecture` (`.docx` / `.pdf`): Detailed technical diagram and architectural walkthrough from intake to fulfillment.

### 4. Project Planning Phase (`Project_Deliverables/4. Project Planning Phase/`)
- `Planning logic` (`.docx` / `.pdf`): Agile estimation logic, Fibonacci scale, Sprint 1 (16 pts) and Sprint 2 (16 pts) calculations, and Velocity calculation (16 pts/sprint).
- `Project Planning Template` (`.docx` / `.pdf`): Product backlog, sprint schedule, team velocity chart, and sprint burndown chart.

### 5. Project Development Phase (`Project_Deliverables/5. Project Development Phase/`)
- `User Acceptance Testing FSD` (`.docx` / `.pdf`): 8 UAT test cases (TC-001 to TC-008, 100% PASS rate) and defect resolution log (BG-001 to BG-003).
- `UAT Report Template` (`.docx` / `.pdf`): Formal UAT execution summary, live execution evidence, and formal sign-off.

### 6. Project Documentation (`Project_Deliverables/6. Project Documentation/`)
- `Automated_Network_Request_Management_Final_Project_Report` (`.docx` / `.pdf`): Comprehensive 11-section project report matching the official SmartBridge Project Report Format with all authentic screenshots embedded.

### 7. Project Demonstration (`Project_Deliverables/7. Project Demonstration/`)
- `Project Demonstration Link & Walkthrough` (`.docx` / `.pdf`): Verified project links, instance metadata, and second-by-second walkthrough of the 13-minute demo video.

---

## 🎥 Live Video Demonstration Breakdown
- **00:00 - 01:15:** Custom Table Schema (`Database Table1` / `u_database_table1`) & column dictionary.
- **01:16 - 02:05:** System Relationship `Approval request1` configuration script.
- **02:06 - 04:10:** Service Catalog Item `Network Request1` & 7 catalog variables.
- **04:11 - 04:35:** Catalog UI Policy `visible/hide of ID field` conditional logic.
- **04:36 - 07:10:** Workflow Studio / Flow Designer actions configuration (`Get Catalog Variables`, `Create Record`, `Send Email`, `Ask for Approval`).
- **07:11 - 09:10:** Flow branching logic (`If Request is approved`) & Catalog Task dispatch.
- **09:11 - 10:20:** Flow runtime execution logs (`sys_flow_context`) with millisecond metrics.
- **10:21 - 11:35:** Service Portal (`/sp`) live order submission by Abraham Lincoln (`REQ0010005` / `RITM0010005`).
- **11:36 - 12:59:** Approval record execution (`sysapproval_approver`), email previews, and fulfillment queue verification.

---

## 📦 Download & Submission
The complete project package is compressed into a single archive:
- **Zip Archive:** `Automated_Network_Request_Management_Pooja_Reddy_Submission.zip`
- **Contains:** All 7 phase directories, 15 Word documents (`.docx`), 15 PDF documents (`.pdf`), high-resolution diagrams, and extracted implementation screenshots.
