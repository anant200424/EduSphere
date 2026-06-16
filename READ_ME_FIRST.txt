╔══════════════════════════════════════════════════════════════╗
║        EduSphere — Complete Student Management System        ║
║          FULL SETUP GUIDE — READ BEFORE RUNNING              ║
╚══════════════════════════════════════════════════════════════╝

  Folder structure:
  com/student/
  ├── util/
  │   └── DBConnect.java
  ├── model/
  │   ├── Student.java
  │   ├── Admin.java
  │   ├── Course.java
  │   └── Payment.java
  ├── dao/
  │   ├── StudentDAO.java
  │   ├── AdminDAO.java
  │   ├── CourseDAO.java
  │   ├── PaymentDAO.java
  │   └── EnrollmentDAO.java
  └── controller/
      ├── LoginServlet.java
      ├── AdminLoginServlet.java
      ├── RegisterServlet.java
      ├── LogoutServlet.java
      ├── AdminLogoutServlet.java
      ├── ForgotPasswordServlet.java
      ├── AdminForgotPasswordServlet.java
      ├── PaymentServlet.java
      ├── EnrollmentServlet.java
      ├── StudentServlet.java
      ├── AdminCourseServlet.java
      └── AdminEnrollmentDeleteServlet.java


 StudentManagement_Enhanced/src/main/webapp/
  home.jsp               ← Landing page
  login.jsp              ← Student login
  register.jsp           ← Student registration
  adminLogin.jsp         ← Admin login
  forgotPassword.jsp     ← Student forgot password
  resetPassword.jsp      ← Student reset password
  adminForgotPassword.jsp← Admin forgot password
  adminResetPassword.jsp ← Admin reset password
  studentDashboard.jsp   ← Student main dashboard
  payFees.jsp            ← Razorpay payment page
  paymentHistory.jsp     ← Student payment history
  myEnrollments.jsp      ← Student's enrolled courses
  enrollCourse.jsp       ← Browse & enroll courses
  aiPredict.jsp          ← AI performance predictor
  adminDashboard.jsp     ← Admin main dashboard
  manageStudents.jsp     ← Admin manage students
  editStudent.jsp        ← Admin edit student
  adminPayments.jsp      ← Admin all payments
  adminEnrollments.jsp   ← Admin all enrollments
  adminCourses.jsp       ← Admin manage courses

HOME PAGE (home.jsp)
├── Student Login (login.jsp)
│   ├── Forgot Password (forgotPassword.jsp)
│   │   └── Reset Password (resetPassword.jsp)
│   └── Register (register.jsp)
│
├── Student Dashboard (studentDashboard.jsp) [after login]
│   ├── Enroll Course (enrollCourse.jsp)
│   ├── My Enrollments (myEnrollments.jsp)
│   ├── Pay Fees (payFees.jsp) [Razorpay]
│   ├── Payment History (paymentHistory.jsp)
│   └── AI Predictor (aiPredict.jsp) [Python ML]
│
└── Admin Login (adminLogin.jsp)
    ├── Admin Forgot Password (adminForgotPassword.jsp)
    │   └── Admin Reset Password (adminResetPassword.jsp)
    └── Admin Dashboard (adminDashboard.jsp) [after login]
        ├── Manage Students (manageStudents.jsp)
        │   └── Edit Student (editStudent.jsp)
        ├── All Enrollments (adminEnrollments.jsp)
        ├── Manage Courses (adminCourses.jsp)
        └── All Payments (adminPayments.jsp)

════════════════════════════════════════════════════════════════
                  COMMON ERRORS & FIXES
════════════════════════════════════════════════════════════════

ERROR: 404 Not Found
FIX: URL must be http://localhost:8080/StudentManagement_Enhanced/home.jsp
     (Use exact project name shown in Eclipse)

ERROR: Red squiggly lines in Eclipse
FIX: Right-click project → Maven → Update Project → OK

ERROR: DB Connection Failed in console
FIX: Check MySQL is running + password in DBConnect.java is correct

ERROR: 500 Internal Server Error
FIX: Check Tomcat console tab — look for the error message
     Usually means DB not connected

ERROR: import javax.servlet cannot be resolved
FIX: pom.xml has been fixed to use jakarta.servlet — redo Maven update

ERROR: ClassNotFoundException mysql driver
FIX: Make sure pom.xml is replaced and Maven updated

════════════════════════════════════════════════════════════════
           SOME INTRO ABOUT THIS PROJECT
════════════════════════════════════════════════════════════════

"This project is a full-stack Student Management System built using
Java Servlets and JSP for the MVC architecture, JDBC with MySQL for
database operations using the DAO pattern, Jakarta EE on Apache Tomcat
10.1, Razorpay payment gateway for online fee collection with webhook
integration, and a Python Flask microservice with a machine learning
performance prediction algorithm. The frontend uses Bootstrap 5,
Chart.js for analytics dashboards, and Google Fonts. The system
supports role-based access with separate Student and Admin portals,
complete CRUD operations, course enrollment, payment tracking, and
AI-powered academic performance prediction."

════════════════════════════════════════════════════════════════
