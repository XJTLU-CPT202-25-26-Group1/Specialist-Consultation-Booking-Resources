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
As an administrator, I want to review "Pending" booking requests so that I can officially confirm or reject the specialist's schedule based on their actual availability.

**Acceptance Criteria**
1. GIVEN a booking is in "Pending" status, WHEN I access the request, THEN the system must provide options to either "Confirm" or "Reject".
2. GIVEN a booking is in "Pending" status, WHEN I click "Confirm", THEN the system must update the status to "Confirmed".
3. GIVEN a status update to "Confirmed" is successful, WHEN the confirmation is processed by the system, THEN an automated notification must be sent to the Customer.
4. GIVEN I choose to reject a booking, WHEN I attempt to submit the rejection, THEN the system must verify that the "Reason for Rejection" field is not empty.
5. GIVEN a valid rejection reason is provided, WHEN I confirm the action, THEN the status must transition to "Cancelled".
6. GIVEN the rejection process is finalized, WHEN the record is saved, THEN the "Reason for Rejection" text must be permanently linked to that specific booking.

---

## PBI 2: Booking Cancellation

**User Story**  
As a customer, I want to cancel my confirmed bookings so that I can manage my schedule and release resources I no longer need.

**Acceptance Criteria**
1. GIVEN a booking is in "Confirmed" status, WHEN I view their dashboard, THEN the "Cancel" option should be accessible.
2. GIVEN the current time is more than 24 hours before the appointment start time, WHEN I click "Cancel", THEN the status must change to "Cancelled".
3. GIVEN the appointment is scheduled within the next 24 hours, WHEN I access the booking, THEN the system must disable the "Cancel" button.
4. GIVEN a restricted cancellation window (< 24 hours), WHEN I hover over or clicks "Cancel", THEN the error message "Cancellations within 24 hours must be handled by an administrator" must be displayed.
5. GIVEN a successful cancellation, WHEN the status is updated, THEN the previously occupied timeslot must be set back to "Available" for other users.

---

## PBI 3: Booking Rescheduling

**User Story**  
As a customer, I want to modify the date and time of my existing booking so that I can adjust my consultation plan without re-entering all details.

**Acceptance Criteria**
1. GIVEN a "Confirmed" booking, WHEN I enter "Edit Mode", THEN the system must allow modification of the date and time fields.
2. GIVEN the current time is more than 24 hours before the appointment start time, WHEN I attempt to reschedule, THEN the system must permit access to the date/time picker.
3. GIVEN the appointment is scheduled within the next 24 hours, WHEN the I view the booking, THEN the system must disable the "Edit/Reschedule" option and display a message: "Rescheduling within 24 hours must be handled by an administrator.
4. GIVEN I select a new date or time, WHEN the system validates the request, THEN it must check if the new slot is currently "Available" in the specialist's schedule.
5. GIVEN a valid new timeslot is chosen, WHEN I click "Submit", THEN the system must save the new timestamp to the booking record.
6. GIVEN the update is successful, WHEN the record is refreshed, THEN the old timeslot must be released and marked as "Available".
7. GIVEN the rescheduling is complete, WHEN the process finishes, THEN a confirmation of the new schedule must be visible to the user.

---

## PBI 4: Booking Status Management and Record Locking

**User Story**  
As an administrator, I want to manage the full transition of booking statuses (Pending, Confirmed, Cancelled, Completed) and lock finalized records.

**Acceptance Criteria**
1. GIVEN a booking exists, WHEN the status transition begins, THEN the system must verify whether this change complies with the permitted workflow. 
2. GIVEN any status change occurs, WHEN the record is updated, THEN the system must log a timestamp and the unique User ID of the person who made the change.
3. GIVEN a booking has reached a terminal state ("Cancelled" or "Completed"), WHEN any user attempts to change the status field again, THEN the system must block the update.
4. GIVEN a booking is in a terminal state, WHEN a status update is blocked, THEN the system must return a "Record Locked" error message.
5. GIVEN a booking is "Cancelled" or "Completed", WHEN an Administrator needs to update non-status fields (e.g., internal notes), THEN the system should allow these modifications while keeping the status locked.

---

## PBI 5: Automated Fee Calculation

**User Story**  
As an Administrator, I want the system to automatically calculate fees based on specialist so that pricing remains consistent and error-free.

**Acceptance Criteria**
1. GIVEN a specialist is booked, WHEN the system initializes price view, THEN it must retrieve the corresponding hourly rate from the fee schedule.
2. GIVEN the rate and duration are known, WHEN the fee is calculated, THEN the system must display the total using the formula " hourly rate x time".
3. GIVEN the status is changed to "Completed", WHEN the final price is generated, THEN the system must send the total charge to the booking ID.
4. GIVEN the fee is calculated, WHEN I view the record, THEN the record of the calculation must be visible for audit purposes.

---

## Summary
Module 5 governs the full booking lifecycle, ensuring that all operations follow strict business rules. It maintains data consistency through controlled status transitions, enforces time-based constraints, protects finalized records, and guarantees accurate fee calculation.
