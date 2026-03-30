# Specialist Consultation Booking System

## 📌 Project Overview
This project develops a web-based booking system for a consultancy service provider.  
Customers can browse specialists, check available consultation slots, and create bookings.  
Administrators manage specialists, availability, bookings, and pricing.

The system supports the full booking workflow:
**booking → confirmation → cancellation/rescheduling → completion**

---

## 👥 Main User Roles
- **Administrator / Operations Manager**
- **Specialist**
- **Customer**

---

## ⚙️ Core Functional Requirements

### A. User and Access Management
- User registration, login, and logout
- Profile maintenance

### B. Specialist and Availability Management
- Manage specialist records (name, expertise, level, fee, status)
- Maintain available consultation slots
- Search and filter specialists by expertise, level, and availability

### C. Booking Workflow
- Customers create bookings by selecting specialist, date/time slot, and notes
- Conflict detection (prevent double booking)
- Booking status management: Pending, Confirmed, Cancelled, Completed
- Confirmation and rejection of bookings
- Cancellation and rescheduling (with constraints)
- Automatic fee calculation

### D. Specialist and Customer Views
- Specialist schedule view
- Specialist marks appointments as completed
- Customer booking history and tracking

### E. Administration
- Manage expertise categories (master data)

---

## 📚 System Modules

The system is divided into 8 modules:

1. User Access and Personal Information Management  
2. Specialist Information Management  
3. Specialist Availability Management  
4. Booking Request Creation and Validation  
5. Booking Workflow and Status Management  
6. Specialist Consultation and Feedback Management  
7. Customer Booking and Tracking  
8. Expertise Category Management  

---

## 🔗 Detailed Requirements (PBIs)

Each module is broken down into Product Backlog Items (PBIs), including user stories and acceptance criteria.

- [Module 1 - User Access](MODULE and PBI/docs/module1-user-access.md)
- [Module 2 - Specialist Management](MODULE and PBI/docs/module2-specialist-management.md)
- [Module 3 - Availability Management](MODULE and PBI/docs/module3-availability.md)
- [Module 4 - Booking Request](MODULE and PBI/docs/module4-booking-request.md)
- [Module 5 - Booking Workflow](MODULE and PBI/docs/module5-booking-workflow.md)
- [Module 6 - Consultation & Feedback](MODULE and PBI/docs/module6-consultation-feedback.md)
- [Module 7 - Customer Booking](MODULE and PBI/docs/module7-customer-booking.md)
- [Module 8 - Expertise Category](MODULE and PBI/docs/module8-expertise-category.md)

---

## 🚀 Current Sprint
**Current Focus (Mar 30 – Apr 5):**
- Finalize requirements documents
- Improve README structure
- Confirm system roles and business rules

---

## 📅 Project Backlog (Mar 30 – May 5)

Tasks will be updated from `[ ]` to `[x]` once completed.

---

### Phase 1: Requirements Analysis and Planning (Mar 30 – Apr 5)
- [x] Define project scope and workflow
- [x] Identify system modules
- [x] Write PBIs
- [x] Organize requirement documents
- [ ] Finalize README
- [ ] Review module boundaries
- [ ] Confirm business rules

---

### Phase 2: Backend Foundation (Apr 6 – Apr 12)
- [ ] Initialize Spring Boot project
- [ ] Set up project structure
- [ ] Configure MySQL database
- [ ] Design database schema
- [ ] Create core entities (User, Specialist, Booking, Slot, Category)

---

### Phase 3: User & Specialist Management (Apr 13 – Apr 19)
- [ ] Implement user registration/login
- [ ] Implement profile management
- [ ] Implement specialist CRUD
- [ ] Implement category management
- [ ] Implement search/filter

---

### Phase 4: Booking Core Features (Apr 20 – Apr 26)
- [ ] Implement availability slots
- [ ] Implement slot conflict detection
- [ ] Implement booking creation
- [ ] Implement validation
- [ ] Prevent double booking

---

### Phase 5: Booking Workflow & Views (Apr 27 – May 1)
- [ ] Implement confirmation/rejection
- [ ] Implement cancellation/rescheduling
- [ ] Implement booking status transitions
- [ ] Implement specialist view
- [ ] Implement customer tracking
- [ ] Implement fee calculation

---

### Phase 6: Testing & Finalization (May 2 – May 5)
- [ ] End-to-end testing
- [ ] Fix bugs
- [ ] Improve validation
- [ ] Clean code
- [ ] Add screenshots/demo
- [ ] Final submission

---

## 📊 Progress Tracking
- Current Phase: Phase 1
- Status: In Progress 🚧

---

## 📌 Business Rules
- A slot cannot be booked by more than one customer
- Only confirmed bookings are valid appointments
- Completed bookings cannot be modified
- Pricing must follow defined rules consistently

---

## 🛠️ Tech Stack (Planned)
- Backend: Spring Boot
- Database: MySQL
- Frontend: (optional / basic UI)
- API Testing: Postman

---

## 📖 Development Approach
This project follows Scrum principles.  
All functionalities are decomposed into PBIs with clear user stories and acceptance criteria, enabling incremental development and continuous improvement.
