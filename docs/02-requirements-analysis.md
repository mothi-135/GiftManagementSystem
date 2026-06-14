# Requirements Analysis

## Stakeholders

### Primary Stakeholders

* Global Admin
* HR Admin
* HR User
* Employee
* Issuer
* Facilities User
* Security User

### Secondary Stakeholders

* Management Team
* IT Support Team

---

# Business Requirements

BRQ-001: The organization shall manage gift distribution through a centralized application.

BRQ-002: The application shall support employee enrolment for gift events.

BRQ-003: The application shall support QR-based gift issuance.

BRQ-004: The application shall maintain inventory records.

BRQ-005: The application shall provide reporting and MIS capabilities.

BRQ-006: The application shall maintain audit logs for critical operations.

BRQ-007: The application shall support role-based and location-based access control.

---

# Functional Requirements

## Authentication & Authorization

* User Login
* User Logout
* Password Management
* Role-Based Access Control
* Location-Based Access Control

## User Management

* Create User
* Update User
* Activate User
* Deactivate User
* Assign Roles
* Assign Locations

## Master Data Management

* Location Master
* Employee Master
* Department Master
* Designation Master
* Category Master
* Unit Master
* Grade Master
* Financial Year Master

## Gift Event Management

* Create Gift Event
* Edit Gift Event
* Initiate Gift Event
* Close Gift Event
* Reopen Gift Event

## Gift Item Management

* Create Gift Item
* Configure Combo Gifts
* Associate Gifts with Events

## Employee Targeting

* Upload Employee List
* Select Employees from Master
* Manage Eligibility

## Email Management

* Configure Email Templates
* Send Notifications
* Maintain Email Logs

## Employee Enrolment

* View Active Events
* Select Gift Preferences
* Submit Enrolment
* Withdraw Enrolment

## QR Management

* Generate QR Code
* Validate QR Code

## Gift Issuance

* Scan QR Code
* Validate Eligibility
* Issue Gift
* Withdraw Gift
* Reissue Gift

## Inventory Management

* Allocate Stock
* Track Consumption
* Update Inventory
* View Stock Status

## Reporting

* Event Summary Report
* Employee Gift History Report
* Event-wise Issuance Report
* Location-wise Distribution Report
* Pending Issuance Report
* Withdrawn Gift Report
* Stock Report
* Audit Trail Report
* Department-wise Report
* Financial Year Report

## Audit Trail

* Capture Create Operations
* Capture Update Operations
* Capture Delete Operations
* Capture Issuance Activities
* Capture Withdrawal Activities
* Capture Reissue Activities

---

# Non Functional Requirements

## Security

* Authentication required
* Role-based access control
* Location-based access control
* Audit logging

## Performance

* Responsive user experience
* Efficient QR validation
* Fast report generation

## Reliability

* Accurate stock management
* Consistent issuance tracking

## Scalability

* Support organization-wide deployments
* Handle large employee datasets

## Maintainability

* Modular architecture
* Layered design approach

## Auditability

* Complete transaction history
* User activity tracking

---

# Validation Requirements

## Gift Event Validation

* Gift Name is mandatory
* Financial Year is mandatory
* Start Date is mandatory
* End Date is mandatory
* End Date cannot be earlier than Start Date
* Location is mandatory
* At least one gift item must exist
* At least one target employee must exist
* Email template must exist before initiation

## Employee Enrolment Validation

* Employee must be eligible
* Event must be initiated
* Enrolment must occur within valid dates
* Gift preferences must be selected
* Duplicate enrolment is prohibited
* Withdrawn employees cannot receive gifts

## Issuance Validation

* Event must be in Issuance status
* QR must be valid
* Employee must be enrolled
* Gift must not already be issued
* Stock must be available
* Issuer must belong to event location
* Timestamp and issuer details must be captured

---

# Event Status Lifecycle

Created → Initiated → Issuance → Closed

Special Transition:

Closed → Reopen (Global Admin Only)

---

# Employee Gift Status Lifecycle

Eligible → Enrolled → Pending → Issued

Alternative States:

* Withdrawn
* Reissued
* Closed

---

# Assumptions

* Employee master data will be available.
* Email service will be provided.
* Browser QR scanning is supported.
* Initial version will be web-based.
* Employee identification data is available.

---

# Dependencies

* PostgreSQL Database
* SMTP Service
* Employee Master Data
* Location Data
* QR Generation Library
* Excel Import Library
* Report Export Library

---

# Constraints

* PERN Stack Architecture
* MVC Pattern
* PostgreSQL Database
* JWT Authentication
* Docker-Based Deployment
* Role-Based Access Control
* Audit Logging

---

# Risks

## Data Quality Risk

Incorrect employee master data may impact eligibility.

## Inventory Risk

Incorrect stock updates may affect gift issuance.

## QR Validation Risk

Invalid QR handling may cause distribution issues.

## Email Delivery Risk

SMTP issues may prevent event notifications.

## Security Risk

Unauthorized access if RBAC is incorrectly implemented.
