# Module 7: Customer Booking and Tracking

## Overview
This module allows customers to view, track, and manage their bookings. It provides clear access to booking history, current status, upcoming appointments, and detailed booking information.

## Primary Stakeholders
- Customer

## Operational Context
Customers need a clear and reliable way to monitor their bookings. They may want to review past consultations, check the current status of bookings, view upcoming appointments, and access detailed information.  
The system must present accurate and consistent data, handle missing or invalid information, and support efficient search functionality.

---

## PBI 1: View Booking History

**User Story**  
As a customer, I want to view my booking history, so that I can track all my past and current appointments.

**Acceptance Criteria**
1. GIVEN booking records exist, WHEN the customer accesses the booking history page, THEN the system displays a list including date, specialist, and status.
2. GIVEN no booking records exist, WHEN the page is opened, THEN the system displays a “No bookings found” message.
3. GIVEN booking data is loaded, WHEN displayed, THEN records are ordered by date in descending order.
4. GIVEN a system error occurs during loading, WHEN the page is accessed, THEN the system displays an error message and allows retry.

---

## PBI 2: Track Booking Status

**User Story**  
As a customer, I want to track the status of my bookings, so that I know whether they are pending, confirmed, cancelled, or completed.

**Acceptance Criteria**
1. GIVEN a booking exists, WHEN viewing the list, THEN each booking displays its current status.
2. GIVEN a booking status changes, WHEN the page is refreshed, THEN the updated status is shown.
3. GIVEN an invalid or unknown status occurs, WHEN displayed, THEN the system shows a fallback message or error.
4. GIVEN status updates occur concurrently, WHEN displayed, THEN the system ensures consistency without duplicate or conflicting states.

---

## PBI 3: View Upcoming Appointments

**User Story**  
As a customer, I want to view my upcoming appointments, so that I can prepare in advance.

**Acceptance Criteria**
1. GIVEN future bookings exist, WHEN the upcoming section is accessed, THEN only future appointments are displayed.
2. GIVEN no upcoming bookings exist, WHEN accessed, THEN the system displays a “No upcoming appointments” message.
3. GIVEN multiple upcoming bookings exist, WHEN displayed, THEN they are ordered by nearest date.
4. GIVEN a booking time has passed, WHEN the page is refreshed, THEN it is removed from the upcoming list.
5. GIVEN different time zones exist, WHEN displaying time, THEN appointments are shown in the customer’s local time.

---

## PBI 4: Access Booking Details

**User Story**  
As a customer, I want to view detailed booking information, so that I can understand my consultation arrangements.

**Acceptance Criteria**
1. GIVEN a valid booking is selected, WHEN accessed, THEN the system displays details such as specialist name, date, time, and notes.
2. GIVEN some data is missing, WHEN the details page is opened, THEN the system displays available information and indicates missing fields.
3. GIVEN an invalid booking ID is accessed, WHEN processed, THEN the system returns an error message.
4. GIVEN data loading fails, WHEN accessing details, THEN the system displays an error message with retry option.

---

## PBI 5: Search Bookings

**User Story**  
As a customer, I want to search my bookings using keywords, so that I can quickly find specific appointments.

**Acceptance Criteria**
1. GIVEN multiple bookings exist, WHEN a keyword (e.g., specialist name or topic) is entered, THEN matching bookings are displayed.
2. GIVEN the keyword matches different fields, WHEN searching, THEN results are returned based on relevant fields.
3. GIVEN no matches are found, WHEN searching, THEN the system displays a “No results found” message.
4. GIVEN the search input is empty, WHEN submitted, THEN all bookings are displayed.

---

## Summary
Module 7 enhances user experience by providing customers with full visibility and control over their bookings. It ensures that booking information is clear, accessible, and up-to-date, helping users manage their consultations effectively.
