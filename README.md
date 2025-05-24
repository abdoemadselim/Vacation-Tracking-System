# 🌴 Vacation Tracking System

This project is based on the system described in the textbook  
**"Object-Oriented Analysis and Design with Applications" – 3rd Edition**.

The goal is to design and analyze a **Vacation Tracking System** that allows employees to manage leave requests and enables HR and managers to track and act on them efficiently.

---

## 📌 Table of Contents

- [🌴 Vacation Tracking System](#-vacation-tracking-system)
  - [📌 Table of Contents](#-table-of-contents)
  - [🧠 Problem Definition](#-problem-definition)
  - [👓 Vision](#-vision)
  - [📋 Requirements](#-requirements)
    - [Functional requirements (FR):](#functional-requirements-fr)
    - [Non-Functional Requirements (NFR):](#non-functional-requirements-nfr)
  - [🛠 Constraints](#-constraints)
  - [🧠 Requirements Analysis \& Design](#-requirements-analysis--design)
    - [1. Use Case Diagram](#1-use-case-diagram)
    - [2. Use Case-Specific Designs](#2-use-case-specific-designs)
      - [Sequence Diagram](#sequence-diagram)
      - [ER Diagram](#er-diagram)
      - [Flow Chart](#flow-chart)
      - [Pseudocode for the four operations (submit/cancel/withdraw/edit) a leave request](#pseudocode-for-the-four-operations-submitcancelwithdrawedit-a-leave-request)
  - [📄 Use Case Specifications](#-use-case-specifications)
  - [🛠 Technologies](#-technologies)
  - [📚 References](#-references)
---

## 🧠 Problem Definition
Organizations struggle and consume a significant amount of time managing employees leave requests, and it can take days for a leave request to be reviewed and acted upon, causing delays. To address this challenge, an automated vacation tracking system is essential to automate and accelerate this process while saving time and reducing frustration for both employees and the HR team.
## 👓 Vision
A vacation tracking system will provide the employees with an easy way to manage their own vacation time, sick leave without having to be an expert in the company policies. It will help managers track their employees' vacations and availability.
## 📋 Requirements
### Functional requirements (FR): 
1. Employees can submit a leave request with desired start and end date.  
2. Managers (approvers) can approve or reject leave requests, with the option to provide a reason for rejection.  
3. The system must support a fully automated workflow for processing leave requests based on organizational policies.  
4. Employees can view their own leave balance.  
5. HR users can access any relevant data for any employee, including leave balance, carryovers, leave history, etc.  
6. The system must integrate with external HR systems to retrieve employees data for automated workflows.
7. The system must have a notification mechanism (e.g., email, in-app) to:  
    - inform employees when their request is approved/rejected  
    - alert employees about upcoming end-of-leave  
    - notify managers (approvers) of pending requests  
8. The HR team can manually approve or reject requests in special cases (e.g., emergencies or out-of-policy requests).  
9.  The system must support special leave types, such as maternity/paternity leave, with manual intervention by HR.  
10. The system must allow **report generation** for HR (e.g., department-level leave trends, unused leave statistics).  
11. The system must **check for conflicts or overlaps**, such as multiple team members requesting leave at the same time.  
12. The system must track audit logs of leave requests and approvals for accountability and compliance.  
13. The system must allow managers to directly award personal leave time (with system-set limits).  
14. The HR team can update the system leave policies.  

### Non-Functional Requirements (NFR): 
1. The system must be easy to use, with a clean and intuitive UI for both employees and HR/manager users.
2. Employees must be able to access only their own data; access to other employees’ data must be restricted according to roles and permissions.
3. The system must support at least 100 concurrent users without performance degradation.
4. The system must ensure 99% uptime.
5. The system must be accessible on both desktop and mobile devices.
6. The system must ensure role-based access control (RBAC) for different user types (employees, managers, HR).

---

## 🛠 Constraints
1. Is implemented as an extension to the existing intranet portal system, and
uses the portal’s single-sign-on mechanisms for all authentication.
2. The system must work on both mobile and desktop devices with a responsive design.
3. All access and changes to leave data must be logged.
4. Must comply with different regional leave policies and employment contracts.

## 🧠 Requirements Analysis & Design

### 1. Use Case Diagram
  ![Use Case Diagram](./diagrams/useCaseDiagram.png)

### 2. Use Case-Specific Designs
**Use Case: Manage Leave Request**  
#### Sequence Diagram 
  ![Sequence diagram](./diagrams/ManageLeaveRequestuseSequenceDiagrams.png)
#### ER Diagram 
  ![ER diagram](./diagrams/manageLeaveRequestERD.png)
#### Flow Chart
  ![Flow chart](./diagrams/manageLeaveRequestFlowCharts.png)
#### Pseudocode for the four operations (submit/cancel/withdraw/edit) a leave request
  [Pseudocode](./manageLeaveRequestPseudocode.md)


## 📄 Use Case Specifications

| Use Case | Description |
|----------|-------------|
| [`Submit Leave Request`](use-cases-specification/ManageLeaveRequest.md) | Employee submits/cancels/edits a leave request |

---

## 🛠 Technologies

- UML tools: draw.io
- Markdown for documentation

---

## 📚 References

- *Object-Oriented Analysis and Design with Applications*, 3rd Ed – Grady Booch et al.