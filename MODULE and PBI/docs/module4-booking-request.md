# Module 4: Booking Request Creation and Validation

## Overview
This module enables customers to initiate a booking request by searching and selecting suitable specialists and available time slots. It ensures that all booking inputs are valid, complete, and conflict-free before creating an initial booking record.

## Primary Stakeholders
- Customer

## Operational Context
Customers use this module to search for specialists, filter them by expertise and availability, view detailed information, select a suitable time slot, and submit a booking request.  
Before the request is accepted, the system must validate all required inputs, check real-time slot availability, and prevent double booking. Only valid requests are recorded as initial bookings and passed to the booking workflow module.

---

## PBI 1: Search for Bookable Specialists

**User Story**  
As a customer looking for a consultation, I want to search for bookable specialists, so that I can quickly find suitable specialists for my booking request.

**Acceptance Criteria**
1. GIVEN I am on the booking page, WHEN I enter a specialist name or keyword, THEN the system displays matching specialists.
2. GIVEN matching specialists exist, WHEN results are shown, THEN only specialists currently available for booking are listed.
3. GIVEN no specialist matches the search, WHEN results are returned, THEN the system displays a “No matching bookable specialists found” message.

---

## PBI 2: Filter Bookable Specialists by Expertise and Availability

**User Story**  
As a customer choosing a specialist, I want to filter specialists by expertise and availability, so that I can efficiently find suitable options.

**Acceptance Criteria**
1. GIVEN I am viewing specialists, WHEN I select an expertise category, THEN only specialists within that category are displayed.
2. GIVEN I apply a date or time filter, WHEN filtering is executed, THEN only specialists with matching available slots are shown.
3. GIVEN no specialists meet the selected filters, WHEN results are displayed, THEN the system shows a “No suitable specialists available” message.

---

## PBI 3: View Specialist Details and Select an Available Slot

**User Story**  
As a customer preparing to make a booking, I want to view specialist details and select an available time slot, so that I can choose the most appropriate consultation option.

**Acceptance Criteria**
1. GIVEN I select a specialist, WHEN the details page is opened, THEN the system displays the specialist’s profile and available slots.
2. GIVEN available slots exist, WHEN I select a slot, THEN the system marks it as my chosen booking option.
3. GIVEN no slots are available, WHEN viewing the details page, THEN the system indicates that no bookable slots are currently available.

---

## PBI 4: Complete and Validate the Booking Request Form

**User Story**  
As a customer creating a booking request, I want to complete and validate the booking form, so that I can submit accurate and complete booking information.

**Acceptance Criteria**
1. GIVEN I have selected a specialist and slot, WHEN the booking form is opened, THEN the selected information is pre-filled.
2. GIVEN all required fields are completed correctly, WHEN I submit the form, THEN the system accepts the input and proceeds to validation.
3. GIVEN any required field is missing or invalid, WHEN I submit the form, THEN the system rejects submission and displays validation errors.

---

## PBI 5: Prevent Double Booking and Create an Initial Booking Record

**User Story**  
As a customer submitting a booking request, I want the system to prevent double booking and create a valid initial record, so that my request can enter the booking workflow correctly.

**Acceptance Criteria**
1. GIVEN I submit a booking request, WHEN the system performs final validation, THEN it verifies that the selected slot is still available.
2. GIVEN another booking already exists for the same specialist and time slot, WHEN validation is performed, THEN the system rejects the request and notifies that the slot is unavailable.
3. GIVEN all validation checks pass, WHEN the request is saved, THEN the system creates a new booking record with status “Pending”.

---

## Summary
Module 4 is the entry point of the booking process. It ensures that only valid, complete, and conflict-free booking requests are created. By combining search, filtering, selection, validation, and conflict prevention, this module guarantees data consistency and provides a reliable foundation for the booking workflow.
