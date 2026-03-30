# Module 5: Booking Workflow and Status Management

## Overview
This module manages the complete lifecycle of a booking after it is created. It controls status transitions, approval workflows, cancellation and rescheduling rules, record locking, and fee calculation to ensure consistency, reliability, and traceability.

## Primary Stakeholders
- Administrator / Operations Manager
- Customer

## Operational Context
After a booking request is created, it enters a controlled workflow. Administrators review and confirm or reject requests, while customers may cancel or reschedule bookings under specific conditions.  
The system must enforce strict business rules, such as time restrictions, status transitions, and record locking, to maintain data integrity. It also calculates consultation fees and keeps a clear audit trail of all booking activities.

---

## PBI 1: Booking Confirmation and Rejection Workflow

**User Story**  
As an Administrator, I want to review pending booking requests and confirm or reject them, so that bookings reflect actual specialist availability.

**Acceptance Criteria**
1. GIVEN a booking is in "Pending" status, WHEN the Administrator accesses it, THEN the system provides options to “Confirm” or “Reject”.
2. GIVEN the Administrator selects “Confirm”, WHEN the action is completed, THEN the system updates the status to "Confirmed".
3. GIVEN a booking is confirmed, WHEN the update is processed, THEN the system sends a notification to the customer.
4. GIVEN the Administrator selects “Reject”, WHEN submitting the rejection, THEN a reason must be provided.
5. GIVEN a valid rejection is submitted, WHEN processed, THEN the system updates the status to "Cancelled" and stores the rejection reason.

---

## PBI 2: Booking Cancellation

**User Story**  
As a customer, I want to cancel my confirmed bookings, so that I can manage my schedule and release unused time slots.

**Acceptance Criteria**
1. GIVEN a booking is in "Confirmed" status, WHEN the customer views it, THEN a “Cancel” option is available.
2. GIVEN the cancellation is requested more than 24 hours before the appointment, WHEN the customer confirms cancellation, THEN the system updates the status to "Cancelled".
3. GIVEN the appointment is within 24 hours, WHEN the customer attempts cancellation, THEN the system disables the option and displays an error message.
4. GIVEN cancellation is successful, WHEN the status is updated, THEN the associated time slot becomes available again.

---

## PBI 3: Booking Rescheduling

**User Story**  
As a customer, I want to reschedule my booking, so that I can adjust my consultation time without creating a new booking.

**Acceptance Criteria**
1. GIVEN a booking is in "Confirmed" status, WHEN the customer enters edit mode, THEN the system allows modification of date and time.
2. GIVEN the request is more than 24 hours before the appointment, WHEN rescheduling is attempted, THEN the system allows access to available slots.
3. GIVEN the request is within 24 hours, WHEN rescheduling is attempted, THEN the system blocks the action and displays a message.
4. GIVEN a new time slot is selected, WHEN the system validates it, THEN the slot must be available.
5. GIVEN rescheduling is successful, WHEN the update is completed, THEN the old slot is released and the new slot is assigned.

---

## PBI 4: Booking Status Management and Record Locking

**User Story**  
As an Administrator, I want to manage booking status transitions and lock completed records, so that data integrity is maintained.

**Acceptance Criteria**
1. GIVEN a booking exists, WHEN a status change is initiated, THEN the system validates that the transition is allowed (e.g., Pending → Confirmed).
2. GIVEN any status change occurs, WHEN the update is saved, THEN the system records a timestamp and user ID.
3. GIVEN a booking reaches a terminal state ("Cancelled" or "Completed"), WHEN further changes are attempted, THEN the system blocks the update.
4. GIVEN a record is locked, WHEN modification is attempted, THEN the system displays a “Record Locked” error message.

---

## PBI 5: Automated Fee Calculation

**User Story**  
As an Administrator, I want the system to automatically calculate consultation fees, so that pricing remains consistent and accurate.

**Acceptance Criteria**
1. GIVEN a specialist level is identified, WHEN the booking is processed, THEN the system retrieves the corresponding rate.
2. GIVEN the consultation duration is known, WHEN the fee is calculated, THEN the system applies the formula “Rate × Duration”.
3. GIVEN a booking reaches "Completed" status, WHEN final processing occurs, THEN the system calculates and stores the final fee.
4. GIVEN the fee is calculated, WHEN viewed, THEN a detailed breakdown is available for auditing.

---

## Summary
Module 5 governs the full booking lifecycle, ensuring that all operations follow strict business rules. It maintains data consistency through controlled status transitions, enforces time-based constraints, protects finalized records, and guarantees accurate fee calculation.
