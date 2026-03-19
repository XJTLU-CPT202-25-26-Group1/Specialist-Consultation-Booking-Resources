## Specialist Consultation Booking System  
**CPT202 Software Engineering Group Project | Option B**  
### 📖 Project Overview  
- A web-based specialist consultation booking platform that enables customers to browse specialists, check available time slots, and make appointments. The system supports complete booking workflow management and role-based access control.  
- Supervisor: Soon Phei Tin  
- Module: CPT202 Software Engineering Group Project  
  
## ✨ Core Features  
### 🔐 User & Access Control  
- User registration, login, logout  
- Role-based permission: Administrator / Specialist / Customer  
- Personal profile management  
    
### 👨‍⚕️ Specialist & Availability  
- Specialist information management (name, expertise, level, fee)  
- Time slot maintenance  
- Search & filter by expertise, level, availability  
   
### 📅 Booking Workflow  
- Booking creation with specialist, date, time slot, notes  
- Conflict detection to avoid double booking  
- Status flow: Pending → Confirmed → Cancelled / Completed  
- Booking confirmation, rejection, cancellation, rescheduling  
- Automatic price calculation  
    
### 📊 Views & Administration  
- Specialist schedule view  
- Customer booking history & status tracking  
- Master data & category management  
- Basic reporting  
   
### 📏 Business Rules  
- One time slot can only be booked by one customer  
- Only confirmed bookings are valid  
- Completed bookings cannot be modified by customers  
- Pricing follows unified rules  
- Specialists manage their own schedules only  
   
### 🛠️ Tech Stack  
- Frontend: HTML, CSS, JavaScript  
- Backend: (Fill in your stack)  
- Database: MySQL    
- Version Control: Git & GitHub  
- Testing: Manual test cases, demo scenarios  
  
### 📂 Project Structure   
/  
├── frontend/        # Front-end pages and logic  
├── backend/         # Back-end API and services  
├── database/        # SQL scripts, ERD, initialization  
├── docs/            # Requirements, design, reports  
├── test/            # Test cases and evidence  
└── README.md  
  
### 🚀 Workflow  
- Customer browses specialists and selects slot  
- Submit booking → system checks conflict  
- Admin / specialist confirms or rejects  
- Customer tracks booking status  
- Specialist marks appointment as completed  
- System records history for management  
  
### 📦 Deliverables  
- Software Requirements Analysis (Assignment 1)  
- Group Report & Presentation (Assignment 2)  
- Final Individual Report (Assignment 3)  
- Working system + test evidence  
  
### 👥 Team Information  
- Group Number: Group 1  
- TA: Xinyi Zeng  
- Team Members:  
Dong Linhua    
Huang Tongdan   
Peng Yuhan   
Shi Daizong   
Wang Zihan  
Wu Yutong  
Yuan Ziyi   
Zhang Zhanhao   
Chen Pinzheng   
  
### 📌 Notes   
- Implement core functions first; advanced features optional   
- Provide complete test cases and demo evidence     
- Follow software engineering process: requirements, design, sprint, Git, testing
