# Module 3: Specialist Availability Management

## Overview
This module allows specialists to manage their available consultation time slots. It ensures that availability schedules are accurate, non-conflicting, and reliable for booking purposes.

## Primary Stakeholders
- Specialist

## Operational Context
Specialists need to create, update, and manage their availability so that customers can book appointments based on real schedules. The system must prevent overlapping time slots, restrict modification of booked slots, and allow specialists to clearly view their availability.

---

## PBI 1: Create Specialist Available Time Slots

**User Story**  
As a specialist, I want to create available time slots, so that customers can book appointments during my free time.

**Acceptance Criteria**
1. GIVEN the specialist is logged in, WHEN valid date and time are entered, THEN a new availability slot is created successfully.
2. GIVEN the entered time slot overlaps with an existing slot, WHEN submitted, THEN the system rejects it and displays a conflict error.
3. GIVEN the end time is earlier than the start time, WHEN submitted, THEN the system displays a validation error.

---

## PBI 2: Edit or Delete Existing Availability Slots

**User Story**  
As a specialist, I want to edit or delete my availability slots, so that I can keep my schedule up to date.

**Acceptance Criteria**
1. GIVEN a slot is not booked, WHEN the specialist edits it, THEN the system updates the slot successfully.
2. GIVEN a slot is already booked, WHEN the specialist attempts to edit or delete it, THEN the system prevents the action and displays an error.
3. GIVEN a slot is unreserved, WHEN deletion is confirmed, THEN the slot is removed from the schedule.

---

## PBI 3: Check and Prevent Slot Time Conflicts

**User Story**  
As a specialist, I want the system to prevent overlapping time slots, so that my schedule remains consistent.

**Acceptance Criteria**
1. GIVEN an existing slot exists, WHEN a new slot overlaps partially or fully, THEN the system rejects the new slot.
2. GIVEN no conflict exists, WHEN a slot is created, THEN the system accepts the slot.

---

## PBI 4: Lock Booked Slots from Modification

**User Story**  
As a specialist, I want booked slots to be locked, so that confirmed appointments cannot be altered.

**Acceptance Criteria**
1. GIVEN a slot has a confirmed booking, WHEN the specialist tries to edit it, THEN the system blocks the action.
2. GIVEN a slot has a completed booking, WHEN modification is attempted, THEN the system denies the request.

---

## PBI 5: View Specialist Availability Schedule

**User Story**  
As a specialist, I want to view my availability schedule, so that I can manage my time effectively.

**Acceptance Criteria**
1. GIVEN the specialist is logged in, WHEN accessing the schedule page, THEN all availability slots are displayed.
2. GIVEN there are both booked and free slots, WHEN viewing the schedule, THEN each slot clearly shows its status.

---

## Summary
Module 3 ensures that specialists can effectively manage their availability while maintaining scheduling integrity. It prevents conflicts, protects booked slots, and provides a clear view of time allocations, forming a reliable basis for booking operations.
