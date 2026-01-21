```mermaid
usecaseDiagram

actor Student
actor Faculty
actor Admin

rectangle "University Management System" {

  %% =====================
  %% Authentication
  %% =====================
  (Login) as UC_Login
  (Signup) as UC_Signup
  (Logout) as UC_Logout

  Student --> UC_Login
  Student --> UC_Signup
  Faculty --> UC_Login
  Admin --> UC_Login

  Student --> UC_Logout
  Faculty --> UC_Logout
  Admin --> UC_Logout

  %% =====================
  %% Student Use Cases
  %% =====================
  (View Dashboard) as UC_StudentDashboard
  (Update Profile) as UC_UpdateProfile
  (Course Registration) as UC_CourseReg
  (View Attendance) as UC_ViewAttendance
  (View Grades & GPA) as UC_ViewGrades
  (Apply for Leave) as UC_ApplyLeave
  (Request Documents) as UC_RequestDocs
  (View Notifications) as UC_Notifications

  Student --> UC_StudentDashboard
  Student --> UC_UpdateProfile
  Student --> UC_CourseReg
  Student --> UC_ViewAttendance
  Student --> UC_ViewGrades
  Student --> UC_ApplyLeave
  Student --> UC_RequestDocs
  Student --> UC_Notifications

  %% =====================
  %% Faculty Use Cases
  %% =====================
  (Mark Attendance) as UC_MarkAttendance
  (Manage Grades) as UC_ManageGrades
  (Upload Study Material) as UC_UploadMaterial
  (Create Assessments) as UC_CreateAssessments
  (Approve Requests) as UC_ApproveRequests

  Faculty --> UC_MarkAttendance
  Faculty --> UC_ManageGrades
  Faculty --> UC_UploadMaterial
  Faculty --> UC_CreateAssessments
  Faculty --> UC_ApproveRequests

  %% =====================
  %% Admin Use Cases
  %% =====================
  (Manage Users) as UC_ManageUsers
  (Assign Roles & Permissions) as UC_Roles
  (Publish Announcements) as UC_Announcements
  (System Monitoring) as UC_SystemMonitoring

  Admin --> UC_ManageUsers
  Admin --> UC_Roles
  Admin --> UC_Announcements
  Admin --> UC_SystemMonitoring

  %% =====================
  %% Include & Extend
  %% =====================
  UC_StudentDashboard ..> UC_Notifications : <<include>>
  UC_ManageUsers ..> UC_Roles : <<include>>
  UC_ApplyLeave ..> UC_ApproveRequests : <<extend>>
}
