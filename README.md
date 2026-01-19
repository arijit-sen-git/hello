```mermaid
flowchart LR

%% ===== Actors =====
Student([🎓 Student])
Faculty([👨‍🏫 Faculty])
Admin([🧑‍💼 Admin])

%% ===== System Boundary =====
subgraph UMS["University Management System"]

    %% Student Use Cases
    UC1((Login))
    UC2((View Dashboard))
    UC3((Complete Profile))
    UC4((Register / Modify Courses))
    UC5((View Attendance))
    UC6((View Grades & GPA))
    UC7((Apply for Leave))
    UC8((Update Personal Information))
    UC9((Request Documents))
    UC10((Participate in Clubs & Events))
    UC11((View Notifications))
    UC12((Logout))

    %% Faculty Use Cases
    UC13((Mark Attendance))
    UC14((Manage Grades))
    UC15((Upload Study Materials))
    UC16((Create Assessments))
    UC17((Approve Student Requests))
    UC18((Monitor Student Performance))
    UC19((Send Messages & Feedback))

    %% Admin Use Cases
    UC20((Manage Users))
    UC21((Assign Roles))
    UC22((Manage Courses))
    UC23((Generate Reports))
    UC24((System Configuration))

end

%% ===== Relationships =====
Student --> UC1
Student --> UC2
Student --> UC3
Student --> UC4
Student --> UC5
Student --> UC6
Student --> UC7
Student --> UC8
Student --> UC9
Student --> UC10
Student --> UC11
Student --> UC12

Faculty --> UC1
Faculty --> UC13
Faculty --> UC14
Faculty --> UC15
Faculty --> UC16
Faculty --> UC17
Faculty --> UC18
Faculty --> UC19
Faculty --> UC11
Faculty --> UC12

Admin --> UC1
Admin --> UC20
Admin --> UC21
Admin --> UC22
Admin --> UC23
Admin --> UC24
Admin --> UC12
