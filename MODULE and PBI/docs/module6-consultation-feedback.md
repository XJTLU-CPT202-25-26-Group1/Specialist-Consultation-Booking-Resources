# Module 6: Specialist Consultation and Feedback Management

## Overview
This module supports specialists in managing their consultation activities and handling feedback after bookings are completed. It provides visibility of schedules, allows marking consultations as completed, and ensures feedback is properly recorded and accessible.

## Primary Stakeholders
- Specialist

## Operational Context
After bookings are confirmed, specialists need tools to manage their consultation schedules, track completed sessions, and review feedback from customers or peers.  
The system must present booking information clearly, ensure accurate status updates, and support feedback handling while maintaining data integrity and proper access control.

---

## PBI 1: Weekly Schedule View

**User Story**  
As a specialist, I want to view my weekly schedule, so that I can manage my consultation time effectively.

**Acceptance Criteria**
1. GIVEN confirmed bookings exist, WHEN the weekly calendar is opened, THEN bookings are displayed in the correct date and time.
2. GIVEN multiple bookings exist, WHEN the schedule is shown, THEN bookings are visually distinguishable by status (e.g., Pending, Confirmed, Completed, Cancelled).
3. GIVEN no bookings exist, WHEN the calendar is viewed, THEN the system displays a “No bookings scheduled” message.
4. GIVEN the specialist is not logged in, WHEN accessing the schedule, THEN the system denies access.

---

## PBI 2: Mark Booking as Completed

**User Story**  
As a specialist, I want to mark a booking as completed, so that the system accurately reflects consultation progress.

**Acceptance Criteria**
1. GIVEN a booking is in Pending or Confirmed status, WHEN marked as completed, THEN the system updates the status to "Completed".
2. GIVEN a booking is already completed, WHEN modification is attempted, THEN the system blocks the action and displays an error message.
3. GIVEN an invalid booking ID is used, WHEN updating status, THEN the system returns an error message.
4. GIVEN insufficient permissions, WHEN attempting to update status, THEN the system denies the action.

---

## PBI 3: Receive Consultation Feedback

**User Story**  
As a specialist, I want to receive feedback after consultations, so that I can review and improve my service.

**Acceptance Criteria**
1. GIVEN a consultation is completed, WHEN feedback is submitted, THEN the specialist receives a notification and can view the feedback.
2. GIVEN feedback content is empty or invalid, WHEN submitted, THEN the system rejects it with an error message.
3. GIVEN multiple feedback entries exist, WHEN viewed, THEN all valid feedback is displayed in chronological order.
4. GIVEN feedback is retracted or updated, WHEN changes occur, THEN the system reflects updates and maintains a record.

---

## PBI 4: Booking History Review

**User Story**  
As a specialist, I want to review my booking history, so that I can analyze past consultations and interactions.

**Acceptance Criteria**
1. GIVEN past bookings exist, WHEN filters (e.g., date or client) are applied, THEN only matching records are displayed.
2. GIVEN no records match the criteria, WHEN searching, THEN the system displays a “No records found” message.
3. GIVEN booking history is requested, WHEN exporting, THEN the system generates a report containing key booking details.
4. GIVEN an invalid date range is entered, WHEN filtering, THEN the system displays a validation error.

---

## PBI 5: Booking Notifications

**User Story**  
As a specialist, I want to receive notifications for booking updates, so that I can respond to schedule changes promptly.

**Acceptance Criteria**
1. GIVEN a new booking is confirmed, WHEN it is created, THEN the specialist receives a notification.
2. GIVEN a booking is cancelled, WHEN updated, THEN the notification includes the original appointment details.
3. GIVEN a booking is rescheduled, WHEN confirmed, THEN the notification displays the updated date and time.
4. GIVEN notifications are disabled, WHEN events occur, THEN the system respects user settings.

---

## Summary
Module 6 ensures that specialists can effectively manage consultations and feedback. It improves service quality by providing clear schedule visibility, accurate status updates, and structured feedback handling, supporting continuous improvement in specialist performance.
