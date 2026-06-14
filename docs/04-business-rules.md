# Business Rules

## Authentication Rules

BR-001: Only authenticated users may access the application.

BR-002: Users may access functionality only according to assigned roles.

BR-003: Location-based restrictions shall be enforced where applicable.

---

## User Management Rules

BR-004: Only authorized administrators may create or modify users.

BR-005: Users must be assigned at least one role.

BR-006: Users must be assigned to valid locations where applicable.

---

## Gift Event Rules

BR-007: Gift Name is mandatory.

BR-008: Financial Year is mandatory.

BR-009: Event Start Date is mandatory.

BR-010: Event End Date is mandatory.

BR-011: Event End Date must be greater than or equal to Event Start Date.

BR-012: Event Location is mandatory.

BR-013: At least one gift item must exist before event initiation.

BR-014: At least one eligible employee must exist before initiation.

BR-015: Email template must exist before initiation.

BR-016: Only authorized users may initiate events.

BR-017: Closed events cannot be modified.

---

## Employee Eligibility Rules

BR-018: Only targeted employees may participate.

BR-019: Employees must satisfy eligibility criteria.

BR-020: Employees may participate only during valid event periods.

---

## Enrolment Rules

BR-021: Employees may enroll only in initiated events.

BR-022: Duplicate enrolment is prohibited.

BR-023: Required gift preferences must be selected.

BR-024: Enrolment must occur within the enrolment period.

BR-025: Withdrawn enrolments shall not be processed for issuance.

---

## QR Rules

BR-026: Each successful enrolment shall generate one QR code.

BR-027: QR codes must be unique.

BR-028: QR codes may be redeemed only once.

BR-029: Invalid QR codes shall be rejected.

BR-030: Previously used QR codes shall be rejected.

---

## Issuance Rules

BR-031: Event must be in Issuance status.

BR-032: Employee must be enrolled.

BR-033: Gift must not already be issued.

BR-034: Stock must be available before issuance.

BR-035: Issuer must belong to the event location.

BR-036: Issuance timestamp shall be recorded.

BR-037: Issuer identity shall be recorded.

---

## Withdrawal Rules

BR-038: Gifts may be withdrawn by authorized users only.

BR-039: Withdrawn gifts shall be marked accordingly.

---

## Reissue Rules

BR-040: Reissue requires authorization.

BR-041: Reissued transactions shall maintain audit history.

---

## Inventory Rules

BR-042: Inventory shall never become negative.

BR-043: Every stock movement shall be recorded.

BR-044: Issuance shall automatically reduce inventory.

BR-045: Reversal operations shall update inventory accordingly.

---

## Audit Rules

BR-046: All critical operations shall be audit logged.

BR-047: Audit logs shall capture old and new values.

BR-048: Audit logs shall record operator information.

BR-049: Audit logs shall capture timestamps.

BR-050: Audit logs shall capture IP address details.

BR-051: Audit records shall not be editable by standard users.

---

## Reporting Rules

BR-052: Reports shall respect role-based access.

BR-053: Reports shall respect location-based access.

BR-054: Report filters shall be applied before export.

BR-055: Audit reports shall only be accessible to authorized roles.
