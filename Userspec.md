# SRS · Office Inventory Request System · version 1


## § 01 · Introduction

### 1.1 · Purpose
This SRS defines the requirements for the Office Inventory Request System. It is intended for developers, testers, auditors, and stakeholders to understand, build, and validate the system.

### 1.2 · Scope of the Product

- **Product name:** Office Inventory Request System  

- **What the product will do:**  
The system provides a web-based dashboard where users can request office items such as notepads, snacks, slippers, and stationery. Users can submit requests, view their request status, and check available inventory. Admin users can manage stock, review requests, and update inventory.

- **What the product will NOT do:**  
The system will not include supplier integration, payment processing, or automated purchasing. It will not support multi-branch inventory or AI-based predictions in this version.

- **Benefits / goals:**  
- Reduce manual request handling  
- Improve inventory tracking  
- Provide real-time visibility  
- Increase efficiency and transparency  

- **Applicability:**  
Used by office employees and administrators. Accessible via web browsers on desktop and mobile devices.

### 1.3 · Definitions, Acronyms, Abbreviations

| Term | Meaning |
|---|---|
| SRS | Software Requirements Specification |
| UI | User Interface |
| DB | Database |


### 1.4 · References

1. ISO/IEC/IEEE 29148:2018  
2. Internal office inventory guidelines  
3. Manual inventory tracking system  

### 1.5 · Overview of this Document
This document describes the system overview, features, functional and non-functional requirements, and verification methods.

## § 02 · Overall Description

### 2.1 · Product Perspective

This is a standalone web system that replaces manual inventory processes.

- **System interfaces:** Database system  
- **User interfaces:** Web interface  
- **Hardware interfaces:** None  
- **Software interfaces:** Browser, backend server  
- **Communication interfaces:** HTTP/HTTPS  
- **Operations:** Normal and maintenance modes  
- **Site adaptation:** Configurable for different office environments  

### 2.2 · Product Functions

- Submit inventory requests  
- View request status  
- Display inventory items  
- Manage stock (admin)  
- Update inventory levels  


### 2.3 · User Characteristics

| User Class | Description | Expertise | Frequency |
| Admin | Manages inventory and approvals | Expert | Daily |
| User | Requests items | Basic | Weekly |

### 2.4 · Constraints

- Must run on modern web browsers  
- Requires internet connection  
- Must support basic security features  
- Limited to internal office use  


### 2.5 · Assumptions and Dependencies

- Users have internet access  
- System database is available  
- Users have login credentials  

### 2.6 · Apportioning of Requirements

Future versions may include:
- Supplier integration  
- Automated inventory alerts  
- Advanced reporting  


## § 03 · Specific Requirements

### 3.1 · External Interface Requirements

#### 3.1.1 · User Interfaces
- Request form (name, item, quantity, reason)  
- Request status table  
- Inventory display table  
- Admin inventory update form  

#### 3.1.2 · Hardware Interfaces
- Not applicable  

#### 3.1.3 · Software Interfaces
- Database (MySQL/PostgreSQL)  
- Backend server  

#### 3.1.4 · Communications Interfaces
- HTTP/HTTPS protocol  


### 3.2 · Functional Requirements

#### FR-01 · Submit Request
- **Description:** User submits item request  
- **Inputs:** Name, item, quantity, reason  
- **Processing:** Save request as Pending  
- **Outputs:** Display in request table  
- **Preconditions:** User fills form  
- **Postconditions:** Request stored  
- **Error handling:** Show validation error  
- **Priority:** Must  

#### FR-02 · View Request Status
- **Description:** User views request status  
- **Outputs:** Table showing Pending, Approved, Rejected  
- **Priority:** Must  


#### FR-03 · View Inventory
- **Description:** User views available stock  
- **Outputs:** Inventory table  
- **Priority:** Must  

#### FR-04 · Update Inventory (Admin)
- **Description:** Admin updates stock quantity  
- **Inputs:** Item name, quantity  
- **Processing:** Update database  
- **Outputs:** Updated inventory table  
- **Priority:** Must  


### 3.3 · Non-Functional Requirements

#### 3.3.1 · Performance Requirements
- Response time < 2 seconds  
- Support multiple users  


#### 3.3.2 · Safety Requirements
- Prevent data loss  


#### 3.3.3 · Security Requirements
- Basic authentication  
- Role-based access (admin/user)  


#### 3.3.4 · Software Quality Attributes

| Attribute | Requirement |
| Reliability | System should function without errors |
| Availability | 99% uptime |
| Usability | Easy to use interface |
| Portability | Works on browsers |


#### 3.3.5 · Business Rules
- Only admin can update inventory  
- Requests must be approved before stock change  

### 3.5 · Other Requirements

#### Database Requirements
- Store user requests  
- Store inventory data  
- Maintain history  

## § 04 · Verification

| Req ID | Verification Method | Acceptance Criterion |
| FR-01 | Test | Request saved successfully |
| FR-02 | Test | Status displayed correctly |
| FR-03 | Test | Inventory shown correctly |
| FR-04 | Test | Stock updates correctly |


## § 05 · Appendices

### A. Analysis Models
- Use case diagram  
- Flowchart  


### B. Requirements Traceability Matrix

| Req ID | Source | Test Case(s) | Status |

| FR-01 | User Need | TC-01 | Pending |


### C. Issues List
- Login system not implemented  
- No backend connection yet  

### D. Glossary
- Inventory: Stock of items  
- Request: Item demand by user  


## Changelog

- v0.1 · Initial draft · 2026-04-21  

## Sign-off

| Role | Name | Signature | Date |

| Author (BA) | Neten Dema |  | 21/4/2026 |
| Dev Lead |  Tshewang Choden|  |25/4/2023  |
| QA Lead |  Dawa Zangmo|  | 30/4/2026 |
