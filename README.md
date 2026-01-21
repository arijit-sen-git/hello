```mermaid
usecaseDiagram

actor Student
actor Faculty
actor Admin

%% =====================
%% Authentication
%% =====================
(Login)
(Signup)
(Logout)

Student --> (Login)
Student --> (Signup)
Faculty --> (Login)
Admin --> (Login)

Student --> (Logout)
Faculty --> (Logout)
Admin --> (Logout)

%% =====================
%% Student Use Cases
%% =====================
(View Dashboard)
(Update Profile)
(Course Registration)
(View Attendance)
(View Grades & GPA)
(Apply for Leave)
(Request Documents)
(Participate in Clubs)
(Vote in Elections)
(View Notifications)

Student --> (View Dashboard)
Student --> (Update Profile)
Student --> (Course Registration)
Student --> (View Attendance)
Student --> (View Grades & GPA)
Student --> (Apply for Leave)
Student --> (Request Documents)
Student --> (Participate in Clubs)
Student --> (Vote in Elections)
Student --> (View Notifications)

%% =====================
%% Faculty Use Cases
%% =====================
(View Faculty Dashboard)
(Mark Attendance)
(Manage Grades)
(Upload Study Material)
(Create Assessments)
(Approve Requests)
(Monitor Performance)
(Message Students)
(Generate Reports)

Faculty --> (View Faculty Dashboard)
Faculty --> (Mark Attendance)
Faculty --> (Manage Grades)
Faculty --> (Upload Study Material)
Faculty --> (Create Assessments)
Faculty --> (Approve Requests)
Faculty --> (Monitor Performance)
Faculty --> (Message Students)
Faculty --> (Generate Reports)

%% =====================
%% Admin Use Cases
%% =====================
(Manage Users)
(Assign Roles & Permissions)
(Manage Courses & Departments)
(Publish Announcements)
(System Monitoring)
(Backup & Recovery)

Admin --> (Manage Users)
Admin --> (Assign Roles & Permissions)
Admin --> (Manage Courses & Departments)
Admin --> (Approve Requests)
Admin --> (Publish Announcements)
Admin --> (System Monitoring)
Admin --> (Backup & Recovery)

%% =====================
%% Include / Extend
%% =====================
(View Dashboard) ..> (View Notifications) : <<include>>
(View Faculty Dashboard) ..> (View Notifications) : <<include>>
(Manage Grades) ..> (Monitor Performance) : <<include>>

(Apply for Leave) ..> (Approve Requests) : <<extend>>
(Request Documents) ..> (Approve Requests) : <<extend>>
