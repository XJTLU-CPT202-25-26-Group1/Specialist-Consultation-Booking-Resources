# Specialist Consultation Booking System

## Project Overview
The Specialist Consultation Booking System is designed to support the full lifecycle of specialist consultation services, from user registration and specialist management to booking creation, workflow control, consultation completion, feedback, and category administration.

The system is structured into 8 core modules. Each module focuses on a clear set of responsibilities and is further refined into Product Backlog Items (PBIs) to support Scrum-based development.

---

## System Modules and PBIs

### 1. User Access and Personal Information Management
This module provides the account foundation for all user roles, including customers, specialists, and administrators. It supports secure registration, login, password recovery, logout, and profile maintenance.

**Included PBIs:**
- Email-password registration verification
- Registered user account login verification
- Registered user password recovery
- Active logout for logged-in users
- Personal profile self-editing and verification

---

### 2. Specialist Information Management
This module enables administrators or operations managers to maintain specialist records accurately. It ensures that specialist data is complete, valid, searchable, and operationally manageable.

**Included PBIs:**
- Add specialist basic information
- Edit existing specialist information
- Maintain specialist operational status
- Check for duplicate specialist information
- Search and filter specialists in the admin backend

---

### 3. Specialist Availability Management
This module allows specialists to manage their available consultation time slots. It ensures scheduling reliability by preventing overlaps and restricting changes to booked slots.

**Included PBIs:**
- Create specialist available time slots
- Edit or delete existing availability slots
- Check and prevent slot time conflicts
- Lock booked slots from modification
- View specialist availability schedule

---

### 4. Booking Request Creation and Validation
This module supports customers in starting a booking request. It covers specialist searching, filtering, slot selection, form completion, validation, and prevention of double booking before a valid request enters the workflow.

**Included PBIs:**
- Search for bookable specialists
- Filter bookable specialists by expertise and availability
- View specialist details and select an available slot
- Complete and validate the booking request form
- Prevent double booking and create an initial booking record

---

### 5. Booking Workflow and Status Management
This module manages the end-to-end booking process after a request is created. It controls approval, cancellation, rescheduling, status transitions, record locking, and fee calculation.

**Included PBIs:**
- Booking confirmation and rejection workflow
- Booking cancellation
- Booking rescheduling
- Booking status management and record locking
- Automated fee calculation

---

### 6. Specialist Consultation and Feedback Management
This module helps specialists manage consultations after bookings are arranged. It supports schedule visibility, completion updates, feedback handling, booking history review, and notifications.

**Included PBIs:**
- Weekly schedule view
- Mark booking as completed
- Receive consultation feedback
- Booking history review
- Booking notifications

---

### 7. Customer Booking and Tracking
This module provides customers with clear visibility of their bookings. It helps them review history, monitor status, check upcoming appointments, view booking details, and search for specific records.

**Included PBIs:**
- View booking history
- Track booking status
- View upcoming appointments
- Access booking details
- Search bookings

---

### 8. Expertise Category Management
This module supports administrators in maintaining expertise categories used across the system. It ensures category data remains complete, unique, active where needed, and unavailable for selection when inactive.

**Included PBIs:**
- Create a new expertise category
- View the expertise category list
- Update an existing expertise category
- Activate or deactivate an expertise category
- Prevent duplicate expertise category names

---

## Summary
Together, these 8 modules cover the main operational needs of the Specialist Consultation Booking System, including:
- user account management
- specialist information and availability control
- booking request creation and workflow processing
- consultation follow-up and feedback
- customer-side booking tracking
- expertise category administration

This modular structure improves clarity, supports Scrum-based development, and makes the system easier to design, implement, test, and maintain.
