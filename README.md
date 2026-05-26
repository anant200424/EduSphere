╔══════════════════════════════════════════════════════════════╗
║        EduSphere — Complete Student Management System        ║
╚══════════════════════════════════════════════════════════════╝
<img width="1830" height="963" alt="Screenshot 2026-04-03 004504" src="https://github.com/user-attachments/assets/5499fa8d-a2af-42f5-acd2-4da118bf34a3" />
<img width="1881" height="903" alt="Screenshot 2026-04-03 234901" src="https://github.com/user-attachments/assets/423aab4c-448e-4e8d-b4a9-30274dfe6b81" />
<img width="1905" height="1011" alt="Screenshot 2026-04-24 154119" src="https://github.com/user-attachments/assets/be17e25c-be8d-41a2-a2b6-a7d7d424f965" />
<img width="1870" height="899" alt="Screenshot 2026-04-03 213719" src="https://github.com/user-attachments/assets/d46ac6ab-7d4c-4cd7-828c-e7a85175dfe2" />
<img width="1897" height="910" alt="Screenshot 2026-04-03 235229" src="https://github.com/user-attachments/assets/a0d09870-94d0-4002-93ca-3678a063a3b3" />
<img width="1873" height="854" alt="Screenshot 2026-04-03 235644" src="https://github.com/user-attachments/assets/7e782e53-4c37-4579-a8f5-8530f719100f" />





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

════════════════════════════════════════════════════════════════
COMPLETE PAGE MAP — ALL ACCESSIBLE FROM HOME
════════════════════════════════════════════════════════════════

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




