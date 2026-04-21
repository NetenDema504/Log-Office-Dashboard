### Office Inventory System   Version: 1

## Problem
Organizations rely on manual methods like emails and spreadsheets to manage inventory requests, causing delays and confusion. This leads to poor tracking, lack of transparency, and inefficient stock management.

## 3. Persona
**Name:** Selise  
**Role:** Admin Officer  

**Pain Points:**
- No real-time stock
- Duplicate requests
- Manual approvals

## 4. User Stories

### Employee
As an employee, I want to request items and track status so that I avoid delays.

### Admin
As an admin, I want to approve/reject requests and manage stock efficiently.

### 01 · Introduction

### 1.2 · Scope of the Product
This SRS defines the requirements for the Office Inventory System and serves as a guide for its design and development. It is intended for developers, testers, auditors, regulators, and customers to understand and validate the system.

### Product Name: Office Inventory System  

- **What the product will do:**  
The system will allow employees to request office items online and track their request status. Admin users can review, approve, or reject requests and manage inventory in real time. The system improves visibility, reduces delays, and ensures proper stock management.

- **What the product will NOT do:**  
The system will not include vendor purchasing, external supplier integration, or AI-based demand prediction in this phase. It will not support multi-branch inventory syncing.

- **Benefits / Goals:**  
- Faster request processing  
- Better stock control  
- Reduced manual work  
- Improved transparency  
- Better planning and reporting  

- **Applicability:**  
Used by employees and administrators in offices. Can be deployed as a web application on desktop and laptop.

### 1.3 · Definitions, Acronyms, Abbreviations

| Term | Meaning |
|---|---|
| SRS | Software Requirements Specification |
| UI | User Interface |
| API | Application Programming Interface |
| DB | Database |

### 1.4 · References

1. ISO/IEC/IEEE 29148:2018 — Requirements Engineering  
2. Internal Office Inventory Policy  
3. Previous manual inventory records  

### 1.5 · Overview of this Document

This document describes the system overview, features, requirements, and constraints. It helps developers, testers, and stakeholders understand and build the system correctly.


## § 02 · Overall Description

### 2.1 · Product Perspective

This system is a standalone web application replacing manual inventory processes.

- **System interfaces:** Email notifications, database  
- **User interfaces:** Web (desktop & mobile)  
- **Hardware interfaces:** None specific  
- **Software interfaces:** Browser, database (MySQL/PostgreSQL)  
- **Communication interfaces:** HTTP/REST  
- **Operations:** Normal, maintenance  
- **Site adaptation:** Configurable for different offices  

### 2.2 · Product Functions

Main functions include:
- Submit inventory requests  
- Approve or reject requests  
- Update stock automatically  
- View dashboards and reports  
- Send notifications  

### 2.3 · User Characteristics

| User Class | Description | Expertise | Frequency |
|---|---|---|---|
| Admin | Manages inventory | Expert | Daily |
| Employee | Requests items | Basic | Weekly |
| Auditor | Reviews reports | Expert | Monthly |

### 2.4 · Constraints

- Must run on web browsers  
- Must support role-based access  
- Must ensure data security  
- Limited to internal office use  

### 2.5 · Assumptions and Dependencies

- Internet connection is available  
- Users have login access  
- Database server is stable  

### 2.6 · Apportioning of Requirements
Future versions may include:
- Vendor integration  
- AI forecasting  
- Multi-branch support  

## § 03 · Specific Requirements

 3.1 · External Interface Requirements

#### 3.1.1 · User Interfaces
- Simple dashboard  
- Request forms  
- Status indicators (Pending, Approved, Rejected)  
- Notification messages  

#### 3.1.2 · Hardware Interfaces
- Not required  

#### 3.1.3 · Software Interfaces
- Database system (MySQL/PostgreSQL)  
- Backend server (Node.js/Django)  

#### 3.1.4 · Communications Interfaces
- HTTP/HTTPS  
- Secure login system  

---

### 3.2 · Functional Requirements

#### FR-01 · Submit Request
- **Description:** User submits request  
- **Inputs:** Item name, quantity, purpose  
- **Processing:** Save as Pending  
- **Outputs:** Confirmation message  
- **Priority:** Must.

#### FR-02 · Approve Request
- **Description:** Admin approves request  
- **Processing:** Update status and reduce stock  
- **Priority:** Must  

#### FR-03 · Reject Request
- **Description:** Admin rejects request  
- **Outputs:** Feedback message  
- **Priority:** Must  

#### FR-04 · View Dashboard
- **Description:** Users view request status  
- **Priority:** Must  

### 3.3 · Non-Functional Requirements

#### 3.3.1 · Performance
- System should respond within 2 seconds  
- Support multiple users  

#### 3.3.2 · Safety
- Prevent data loss  

#### 3.3.3 · Security
- Login authentication  
- Role-based access  
- Data encryption  

#### 3.3.4 · Software Quality Attributes

| Attribute | Requirement |
|---|---|
| Reliability | System should run without failure |
| Availability | 99% uptime |
| Usability | Easy to use |
| Portability | Works on browsers |

#### 3.3.5 · Business Rules
- Only admin can approve requests  
- Stock must update after approval  

### 3.5 · Other Requirements

#### Database Requirements
- Store users, requests, inventory  
- Maintain request history  

#### Legal / Compliance
- Follow basic data protection rules  

## § 04 · Verification

| Req ID | Method | Acceptance |
|---|---|---|
| FR-01 | Test | Request saved as Pending |
| FR-02 | Test | Stock updated |
| FR-03 | Test | Rejection message shown |

## § 05 · Appendices

### A. Models
- Use case diagrams  
- Flow diagrams  

### B. Traceability Matrix

| Req ID | Source | Test |
|---|---|---|
| FR-01 | User Need | TC-01 |

## Changelog

- v1 Initial Draft  


## Sign-off

| Role | Name | Date |
| Author | Neten Dema | 21/4/2026 |
| Developer | Tshewang Choden |25/4/2026  |
| Tester |Dawa Zangmo  | 30/4/2026 |


