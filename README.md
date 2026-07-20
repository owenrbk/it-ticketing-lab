# Help Desk & IT Support Ticketing Lab

## Project Overview
This project demonstrates a hands-on simulation of an enterprise IT Support Help Desk environment utilizing **Spiceworks Cloud Help Desk**. The purpose of this lab is to replicate the end-to-end lifecycle of IT service requests, practice strict Service Level Agreement (SLA) prioritization, and develop professional, user-facing communications alongside detailed internal technical documentation. 

By acting as both the end-user (generating requests) and the IT Support Agent (triaging and resolving issues), this lab simulates real-world desktop support, identity management, and access control workflows.

## Tools & Environment
*   **Ticketing Platform:** Spiceworks Cloud Help Desk
*   **Core Concepts:** Ticket Lifecycle, SLA Management, Internal Knowledge Documentation, Active Directory/Entra ID Simulation, Customer Service Communication

---

## Ticket Overview
Below is the centralized agent dashboard showing the status, priority levels, and assignments of active and closed service requests handled during this lab.

### Agent Workspace
![Spiceworks Help Desk Dashboard](images/Capture4.PNG)

---

## Lab Scenarios & Resolution Walkthroughs

### Scenario 1: Password Reset & MFA Lockout
*   **Priority:** Medium (User operational block, non-emergency)
*   **User Issue:** End-user locked out of their primary account after multiple incorrect password attempts following vacation. User also acquired a new mobile device and requires an MFA/Authenticator application registration reset.

#### Technical Resolution & Documentation
**Triage:** Ticket assigned to agent; priority escalated to Medium to ensure minimal user downtime.

*Place your screenshot showing the specific ticket details, internal notes, and customer reply here:*
![Scenario 1 Ticket Details](images/Capture.PNG)

---

### Scenario 2: Shared Network Folder Access (Permissions)
*   **Priority:** Low/Medium (Role transition/Onboarding adjustment)
*   **User Issue:** A recently promoted employee requested access to the restricted network share folder (`Finance-Share`) and reported receiving an "Access Denied" error when attempting to pull necessary departmental reporting sheets.

#### Technical Resolution & Documentation
**Triage:** Assigned to agent workflow. Verified management approval for the access modification.

*Place your screenshot showing the access modification ticket lifecycle here:*
![Scenario 2 Ticket Details](images/Capture2.PNG)

---

### Scenario 3: Urgent Employee Offboarding Request
*   **Priority:** High (Security compliance / Time-sensitive SLA)
*   **User Issue:** An urgent request submitted by Human Resources to deprovision an employee account and revoke all corporate infrastructure access exactly at 5:00 PM due to an offboarding action.

#### Technical Resolution & Documentation
**Triage:** Escalated immediately to High priority. Due date set explicitly for 5:00 PM to meet security compliance compliance guidelines.

![Scenario 3 Ticket Details](images/Capture3.PNG)

---

## Core Competencies Demonstrated
*   **SLA Awareness:** Correctly categorized incoming tickets by urgency and business impact, prioritizing data security and operational uptime.
*   **Professional Empathy & Communication:** Maintained clear, accessible, and jargon-free communication when interacting directly with end-users, ensuring a positive customer service experience.
*   **Technical Literacy:** Documented precise, granular troubleshooting steps in internal IT logs to ensure continuity and clarity for cross-functional technical teams.
