 Office Inventory Admin System ·  Version 1

## 01 · Introduction

### 1.1 · Purpose
This SRS defines the requirements for the Admin module of the Office Inventory System. It is intended for developers, testers, and stakeholders to understand and implement admin functionalities.

### 1.2 · Scope of the Product

- **Product name:** Office Inventory Admin System  

- **What the product will do:**  
The admin system provides a dashboard for managing inventory and user requests. Admins can view all requests, approve or reject them, update stock levels, and monitor inventory in real time. It ensures accurate stock control and efficient request processing.

- **What the product will NOT do:**  
The system will not include supplier purchasing, payment handling, or external system integrations in this version. It will not provide AI-based analytics or automation.

- **Benefits / goals:**  
- Efficient request approval process  
- Accurate inventory tracking  
- Reduced manual errors  
- Improved control and monitoring  

- **Applicability:**  
Used by administrators and inventory managers through a web-based interface.

### 1.3 · Definitions, Acronyms, Abbreviations

| Term | Meaning |

| Admin | System administrator |
| UI | User Interface |
| DB | Database |


### 1.4 · References

1. ISO/IEC/IEEE 29148:2018  
2. Office inventory policies  
3. Existing manual tracking system  


### 1.5 · Overview of this Document
This document outlines admin system features, requirements, constraints, and verification methods.

## § 02 · Overall Description

### 2.1 · Product Perspective

The admin system is part of the overall inventory system and controls core operations.

- **System interfaces:** User system, database  
- **User interfaces:** Web dashboard  
- **Hardware interfaces:** None  
- **Software interfaces:** Backend server, database  
- **Communication interfaces:** HTTP/HTTPS  
- **Operations:** Normal and maintenance  
- **Site adaptation:** Configurable settings  


### 2.2 · Product Functions

- View all user requests  
- Approve or reject requests  
- Update inventory stock  
- Monitor inventory levels  
- Provide feedback on requests  

### 2.3 · User Characteristics

| User Class | Description | Expertise | Frequency |
| Admin | Inventory manager | Expert | Daily |


### 2.4 · Constraints

- Must support role-based access  
- Requires secure login  
- Runs on web browsers  
- Limited to internal use  

### 2.5 · Assumptions and Dependencies

- Admin users have valid credentials  
- Database is available  
- Internet connection is stable  

### 2.6 · Apportioning of Requirements

Future versions may include:
- Advanced analytics  
- Automated alerts  
- Integration with suppliers  

## § 03 · Specific Requirements

### 3.1 · External Interface Requirements

#### 3.1.1 · User Interfaces
- Admin dashboard  
- Request management table  
- Inventory update form  
- Status indicators (Approved, Rejected, Pending)  

#### 3.1.2 · Hardware Interfaces
- Not applicable  


#### 3.1.3 · Software Interfaces
- Database system  
- Backend server  


#### 3.1.4 · Communications Interfaces
- HTTP/HTTPS  

### 3.2 · Functional Requirements

#### FR-01 · View Requests
- **Description:** Admin views all requests  
- **Outputs:** List of requests with details  
- **Priority:** Must  

#### FR-02 · Approve Request
- **Description:** Admin approves a request  
- **Processing:** Update status to Approved and reduce stock  
- **Outputs:** Updated request and inventory  
- **Preconditions:** Request exists  
- **Postconditions:** Stock updated  
- **Error handling:** Show error if stock insufficient  
- **Priority:** Must  

#### FR-03 · Reject Request
- **Description:** Admin rejects a request  
- **Outputs:** Status updated with feedback  
- **Priority:** Must  


#### FR-04 · Update Inventory
- **Description:** Admin adds or updates stock  
- **Inputs:** Item name, quantity  
- **Processing:** Update inventory  
- **Outputs:** Updated stock list  
- **Priority:** Must  


#### FR-05 · Monitor Inventory
- **Description:** Admin views current stock levels  
- **Outputs:** Inventory table  
- **Priority:** Must  

### 3.3 · Non-Functional Requirements

#### 3.3.1 · Performance Requirements
- Response time < 2 seconds  
- Handle multiple requests  

#### 3.3.2 · Safety Requirements
- Prevent incorrect stock updates  

#### 3.3.3 · Security Requirements
- Secure admin login  
- Role-based access control  
- Data protection  


#### 3.3.4 · Software Quality Attributes

| Attribute | Requirement |
|---|---|
| Reliability | System should be stable |
| Availability | 99% uptime |
| Usability | Simple admin interface |
| Portability | Browser compatible |

#### 3.3.5 · Business Rules
- Only admin can approve/reject requests  
- Stock must update after approval  
- Cannot approve if stock is insufficient  


### 3.5 · Other Requirements

#### Database Requirements
- Store requests and inventory  
- Maintain transaction logs  

## § 04 · Verification

| Req ID | Verification Method | Acceptance Criterion |

| FR-01 | Test | Requests displayed correctly |
| FR-02 | Test | Approval updates stock |
| FR-03 | Test | Rejection updates status |
| FR-04 | Test | Inventory updates correctly |


## § 05 · Appendices

### A. Analysis Models
- Admin workflow diagram  

### B. Requirements Traceability Matrix

| Req ID | Source | Test Case(s) | Status |
| FR-01 | Admin Need | TC-01 | Pending |

### C. Issues List
- No authentication system yet  
- No backend integration  

### D. Glossary
- Admin: System manager  
- Inventory: Stock data  


## Changelog

- v0.1 · Initial draft · 2026-04-21  


## Sign-off

| Role | Name | Signature | Date |
| Author (BA) | Neten Dema |  | 21/4/2026 |
| Dev Lead |Tshewang Chiden  |  |30/4/2026  |
| QA Lead | Dawa Zangmo |  |  5/5/2026|
