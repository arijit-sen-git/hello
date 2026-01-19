# CS331 Project  
## University Management System  
### UML Use Case Diagram

---

## 1. System Overview

The **University Management System** is a centralized digital platform designed to manage academic and administrative activities for students, faculty, and administrators.  
This UML Use Case Diagram illustrates the interactions between different users (actors) and the system.

---

## 2. Actors

- **Student** – Manages academic and personal activities
- **Faculty** – Handles teaching, assessments, and student interactions
- **Admin** – Manages system-level operations and configurations

---

## 3. UML Use Case Diagram

```mermaid
usecaseDiagram

actor Student
actor Faculty
actor Admin

rectangle "University Management System" {

    %% ======================
    %% Student Use Cases
    %% ======================
    Student --> (Login)
    Student --> (View Dashboard)
    Student --> (Complete Profile)
    Student --> (Register / Modify Courses)
    Student --> (View Attendance)
    Student --> (View Grades & GPA)
    Student --> (Apply for Leave)
    Student --> (Update Personal Information)
    Student --> (Request Documents)
    Student --> (Participate in Clubs & Events)
    Student --> (View Notifications)
    Student --> (Logout)

    %% ======================
    %% Faculty Use Cases
    %% ======================
    Faculty --> (Login)
    Faculty --> (View Dashboard)
    Faculty --> (Mark Attendance)
    Faculty --> (Manage Grades)
    Faculty --> (Upload Study Materials)
    Faculty --> (Create Assessments)
    Faculty --> (Approve Student Requests)
    Faculty --> (Monitor Student Performance)
    Faculty --> (Send Messages & Feedback)
    Faculty --> (Apply for Leave)
    Faculty --> (View Notifications)
    Faculty --> (Logout)

    %% ======================
    %% Admin Use Cases
    %% ======================
    Admin --> (Login)
    Admin --> (Manage Users)
    Admin --> (Assign Roles)
    Admin --> (Manage Courses)
    Admin --> (Generate Reports)
    Admin --> (System Configuration)
    Admin --> (Logout)

    %% ======================
    %% Include Relationships
    %% ======================
    (Register / Modify Courses) ..> (Login) : <<include>>
    (View Attendance) ..> (Login) : <<include>>
    (View Grades & GPA) ..> (Login) : <<include>>
    (Apply for Leave) ..> (Login) : <<include>>
    (Request Documents) ..> (Login) : <<include>>

    (Mark Attendance) ..> (Login) : <<include>>
    (Manage Grades) ..> (Login) : <<include>>
    (Upload Study Materials) ..> (Login) : <<include>>

    (Manage Users) ..> (Login) : <<include>>
    (Assign Roles) ..> (Login) : <<include>>
}
