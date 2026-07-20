# Help Desk & IT Support Ticketing Lab

## Project Overview
This project demonstrates a hands-on simulation of an enterprise IT Support Help Desk environment utilizing **Spiceworks Cloud Help Desk**. The purpose of this lab is to replicate the end-to-end lifecycle of IT service requests, practice strict Service Level Agreement (SLA) prioritization, and develop professional, user-facing communications alongside detailed internal technical documentation. 

By acting as both the end-user (generating requests) and the IT Support Agent (triaging and resolving issues), this lab simulates real-world desktop support, identity management, and access control workflows.

## Tools & Environment
*   **Ticketing Platform:** Spiceworks Cloud Help Desk
*   **Core Concepts:** Ticket Lifecycle, SLA Management, Internal Knowledge Documentation, Active Directory/Entra ID Simulation, Customer Service Communication

---

## Ticket Overview
Below is the centralized agent view showing the status, priority levels, and assignments of the closed service requests handled during this lab.

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
![Scenario 1 Ticket Details](images/Capture2.PNG)

---

### Scenario 2: Shared Network Folder Access (Permissions)
*   **Priority:** Low/Medium (Role transition/Onboarding adjustment)
*   **User Issue:** A recently promoted employee requested access to the restricted network share folder (`Finance-Share`) and reported receiving an "Access Denied" error when attempting to pull necessary departmental reporting sheets.

#### Technical Resolution & Documentation
**Triage:** Assigned to agent workflow. Verified management approval for the access modification.

*Place your screenshot showing the access modification ticket lifecycle here:*
![Scenario 2 Ticket Details](images/Capture3.PNG)

---

### Scenario 3: Urgent Employee Offboarding Request
*   **Priority:** High (Security compliance / Time-sensitive SLA)
*   **User Issue:** An urgent request submitted by Human Resources to deprovision an employee account and revoke all corporate infrastructure access exactly at 5:00 PM due to an offboarding action.

#### Technical Resolution & Documentation
**Triage:** Escalated immediately to High priority. Due date set explicitly for 5:00 PM to meet security compliance compliance guidelines.

![Scenario 3 Ticket Details](images/Capture.PNG)

---

### Scenario 4: Critical Network Degradation & Tier 3 Escalation
*   **Priority:** Critical / Urgent (High business impact, widespread productivity outage)
*   **User Issue:** Received four consecutive tickets and multiple urgent phone calls within a 10-minute window from users across both the Finance and Operations wings on Floor 2. Users report that corporate VoIP desk phones are completely dropping active client calls, and the cloud-based ERP management system is failing to load, displaying "Connection Timed Out" errors.

#### Technical Triage & Proper Handling Workflow
1.  **Pattern Recognition:** Recognized the immediate correlation between multiple distinct users in the same physical area, instantly bypassing time-wasting endpoint troubleshooting (such as rebooting individual laptops or swapping desk phone cables).
2.  **Information Gathering:** Logged into a remote test environment on the affected floor segment to run baseline network diagnostics. Executed a continuous ping (`ping -t`) to the local default gateway, observing **38% packet loss** and severe latency spikes fluctuating between 600ms and 1200ms. 
3.  **Isolating Scope:** Run a `tracert` to the external cloud ERP environment, verifying that the packet drops and latency spikes were originating directly at the Floor 2 intermediate distribution switch stack. Confirmed via the monitoring tools that users on Floor 1 and Floor 3 were operating with 0% packet loss, successfully narrowing the failure domain to Floor 2 infrastructure.
4.  **Professional Escalation:** Compiled the collected metrics, scope boundaries, and log outputs into a highly structured, clear escalation ticket directed to the Network Engineering team.

#### Technical Escalation & Documentation
*   **Internal IT Escalation Notes (Routed to Network Engineering):**
    > *“CRITICAL ESCALATION: Localized network degradation and high packet loss detected on Floor 2 (VLAN 20). Multiple users reporting dropped VoIP calls and ERP timeouts. Tier 1 diagnostics confirm ~38% packet loss and severe latency spikes (600ms–1200ms) originating at the Floor 2 distribution switch (`SW-FL2-DIST-01`). Ping tests to Floor 1 and Floor 3 gateways remain completely nominal (0% loss, <2ms). Endpoint hardware issues ruled out. Escalating to Tier 3 Network Engineering to investigate potential spanning-tree loops, broadcast storms, or hardware interface errors on the switch stack. Keeping ticket ownership open for user communications.”*

**User Message**
"Hi Help Desk,

I need someone to come up to Floor 2 right now. I was right in the middle of an incredibly important end-of-quarter reconciliation call with our primary vendor and my desk phone completely cut out and hung up on them. Now the screen on my phone just says 'Discovering...' and won't give me a dial tone.

On top of that, I am trying to pull up the ERP system to process today's invoice batch, but the web page just spins continuously for a few minutes before giving me a 'Connection Timed Out' error.

I thought it was just my computer, but Mark in the cubicle right next to me (Cube 205) is having the exact same issue and can't load anything either. Is the entire network down today? Please fix this ASAP, we have a hard deadline by 4:00 PM to get these numbers submitted!"


![Scenario 4 Escalation Details](images/Capture7.PNG)
![Scenario 4 Escalation Details](images/Capture7.PNG)

## Core Competencies Demonstrated
*   **SLA Awareness:** Correctly categorized incoming tickets by urgency and business impact, prioritizing data security and operational uptime.
*   **Professional Empathy & Communication:** Maintained clear, accessible, and jargon-free communication when interacting directly with end-users, ensuring a positive customer service experience.
*   **Technical Literacy:** Documented precise, granular troubleshooting steps in internal IT logs to ensure continuity and clarity for cross-functional technical teams.
