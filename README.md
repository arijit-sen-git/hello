# hello

usecaseDiagram
actor Student
actor Faculty
actor Admin

Student --> (Login)
Student --> (View Dashboard)
Student --> (Register Courses)
Student --> (View Attendance)
Student --> (View Grades)
Student --> (Apply Leave)
Student --> (Request Documents)
Student --> (View Notifications)

Faculty --> (Login)
Faculty --> (Mark Attendance)
Faculty --> (Upload Study Material)
Faculty --> (Manage Grades)
Faculty --> (Create Assessments)
Faculty --> (Approve Requests)
Faculty --> (Send Feedback)

Admin --> (Manage Users)
Admin --> (Assign Roles)
Admin --> (Generate Reports)
Admin --> (Manage Courses)

(Register Courses) ..> (Login) : <<include>>
(Apply Leave) ..> (Login) : <<include>>
