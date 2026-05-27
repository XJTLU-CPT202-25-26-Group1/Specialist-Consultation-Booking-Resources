# Xsbooking Scrum Sprint / Iteration Plan

Project: XJTLU Academic Expert Appointment System (Xsbooking)  
Course: CPT202 Software Engineering Group Project  
Team: Group 1  
Individual focus: Backend booking modules, especially Module 4 and Module 5

---

## Sprint 1 / Iteration 1: Infrastructure

Period: Early project stage  
Increment goal: Build the basic system foundation and create a working MVP for registration and login.

### Main Objectives

- Generate the Spring Boot project structure and build configuration.
- Set up the basic layered architecture for controllers, services, repositories, and domain entities.
- Implement authentication and role-based access control using Spring Security.
- Support the three main user roles: Admin, Specialist, and Customer.
- Implement basic login, logout, registration, and initial user-account handling.
- Create the first version of the database schema, including users and core domain entities.
- Store user roles as enum values in user records.

### Main Deliverables

- Spring Boot application scaffold.
- Security configuration for login, logout, and role-based access.
- Initial user table and role model.
- MVP that supports registration and login.
- Basic navigation structure for different user roles.

### My Backend Contribution

- Helped establish backend domain structure used later by booking modules.
- Worked with role and authentication assumptions needed by customer, admin, and specialist booking actions.
- Prepared for later booking access-control rules, such as customer-only booking creation and specialist-only completion.

### Evidence to Capture

- Screenshot of sprint plan or task board for infrastructure tasks.
- Screenshot of login or registration page.
- Screenshot of role-based navigation after login.
- GitHub commits showing early backend or security setup.

---

## Sprint 2 / Iteration 2: Core Functions

Period: Middle project stage  
Increment goal: Implement the main business workflow of the appointment booking system.

### Main Objectives

- Implement expert and academic-area management.
- Support specialist availability-slot creation and display.
- Build the core booking request workflow.
- Allow customers to search and filter bookable specialists.
- Allow customers to view specialist details and select available slots.
- Validate booking request forms on the backend.
- Prevent booking conflicts and double booking.
- Create initial booking records with `PENDING` status.
- Implement admin confirmation and rejection.
- Implement booking cancellation and rescheduling.
- Implement booking status transitions and fee calculation.
- Create basic role-specific UI pages for end-to-end workflow testing.

### Module 4: Booking Request Creation and Validation

Included PBIs:

- Search for bookable specialists.
- Filter bookable specialists by expertise and availability.
- View specialist details and select an available slot.
- Complete and validate the booking request form.
- Prevent double booking and create an initial booking record.

Backend work:

- `CustomerSpecialistController` supports specialist search and detail views.
- `CustomerBookingController` connects customer booking requests to the service layer.
- `BookingService.createBooking` validates specialist, slot, topic, notes, booking overlap, and fee calculation.
- `AvailabilitySlotRepository` supports slot lookup and locking.
- `BookingRepository` supports active-booking and overlap checks.

### Module 5: Booking Workflow and Status Management

Included PBIs:

- Booking confirmation and rejection workflow.
- Booking cancellation.
- Booking rescheduling.
- Booking status management and record locking.
- Automated fee calculation.

Backend work:

- `AdminBookingController` supports pending booking review, confirmation, rejection, and detail view.
- `SpecialistBookingController` supports specialist booking view and completion.
- `BookingService` centralises status-transition rules.
- `BookingAuditLog` records important status changes.
- Repository locking is used for status-changing operations and slot updates.

### Main Deliverables

- Customer specialist search and detail pages.
- Customer booking creation page.
- Customer booking status tracking page.
- Admin booking review and detail pages.
- Specialist booking view and completion page.
- Backend validation for double booking, slot conflict, status transition, and timing restrictions.
- Backend tests for booking creation, rejection, rescheduling, completion, and edge cases.

### My Backend Contribution

- Implemented most backend logic for Module 4 and Module 5.
- Added booking request creation, validation, conflict prevention, and double-booking protection.
- Added admin confirmation/rejection, customer cancellation/rescheduling, specialist completion, status transitions, fee calculation, and audit logging.
- Added and maintained backend tests for booking-service behaviours.

### Evidence to Capture

- Screenshot of booking task board or backlog card.
- Screenshot of customer specialist search page.
- Screenshot of customer create-booking page.
- Screenshot of admin booking review page.
- Screenshot of admin booking detail with audit log.
- Screenshot of customer reschedule page.
- Screenshot of specialist booking detail or completion page.
- Screenshot of GitHub commits between `a10b9e6` and `a1bfc1f`.
- Screenshot of WeChat feedback about the double-booking issue.

---

## Sprint 3 / Iteration 3: Integration, Deployment, and Final Validation

Period: Final project stage  
Increment goal: Integrate modules, fix workflow issues, deploy the system, and prepare for demonstration.

### Main Objectives

- Conduct integration testing across customer, admin, and specialist workflows.
- Fix issues discovered during page testing and teammate feedback.
- Improve UI responsiveness and page usability.
- Configure the deployment environment on Alibaba Cloud ECS.
- Configure database connection and runtime environment for the deployed application.
- Validate the first-release demonstration version.
- Run automated backend tests before final submission.

### Integration and Bug Fixing

- Worked with integration member Shi Daizong to test deployed pages.
- Used teammate feedback to identify workflow problems.
- Fixed the issue where one student could book multiple experts at overlapping times.
- Improved the backend overlap check by checking the customer's active `PENDING` and `CONFIRMED` bookings.
- Added or adjusted tests for booking conflict and time-related edge cases.
- Covered a midnight/cross-day booking-time edge case, increasing the test suite from 40 to 41 tests.

### Deployment and Validation

- Deployed the application to Alibaba Cloud ECS.
- Configured the server runtime and database connection.
- Used the deployed version for integration testing and demonstration preparation.
- Ran the Maven test suite on the server.

Final test result:

```text
Tests run: 41, Failures: 0, Errors: 0, Skipped: 0
BUILD SUCCESS
Finished at: 2026-05-27T15:16:11+08:00
```

### Main Deliverables

- Deployed web application.
- Integrated customer-admin-specialist booking workflow.
- Bug fixes for double-booking and booking-time validation.
- Final backend test result with 41 passing tests.
- Evidence screenshots for final report appendices.

### My Backend Contribution

- Supported final integration by fixing booking workflow issues found during testing.
- Improved conflict detection and time validation.
- Verified backend booking behaviour through automated tests.
- Prepared evidence for backend contribution, including commit history, test result, and workflow screenshots.

### Evidence to Capture

- Screenshot of deployed application home/login page.
- Screenshot of final Maven test result showing 41 tests passed.
- Screenshot of GitHub commit history.
- Screenshot of WeChat or meeting feedback about integration issues.
- Screenshot of Alibaba Cloud deployment or deployed URL if needed.

---

## Summary of Sprint Progress

| Sprint | Main Theme | Main Increment | Relationship to My Work |
| --- | --- | --- | --- |
| Sprint 1 | Infrastructure | Authentication, role-based access, initial schema, MVP login/register | Prepared the backend foundation used by booking modules |
| Sprint 2 | Core Functions | Specialist search, availability, booking creation, validation, status workflow | Main implementation period for Module 4 and Module 5 backend logic |
| Sprint 3 | Integration and Deployment | Cloud deployment, integration testing, bug fixing, final validation | Fixed booking workflow issues and verified 41 passing tests |


