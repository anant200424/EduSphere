╔══════════════════════════════════════════════════════════════╗
║        EduSphere — Complete Student Management System        ║
║          FULL SETUP GUIDE — READ BEFORE RUNNING             ║
╚══════════════════════════════════════════════════════════════╝

LOGIN CREDENTIALS (After setup):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  Student → Email: student@college.edu | Password: student123
  Admin   → Email: admin@college.edu   | Password: admin123

URL AFTER RUNNING:
━━━━━━━━━━━━━━━━━
  http://localhost:8080/StudentManagement_Enhanced/home.jsp

════════════════════════════════════════════════════════════════
STEP 1 — SET UP MYSQL DATABASE
════════════════════════════════════════════════════════════════

1. Open MySQL Workbench (or cmd: mysql -u root -p)
2. Open file: database/database.sql
3. Select all (Ctrl+A) and click Run (lightning bolt)
4. You should see: "studentmanagement" database created

If your MySQL password is different from "Anant@1234":
→ Open: src/main/java/com/student/util/DBConnect.java
→ Change line: private static final String PASSWORD = "Anant@1234";
→ Replace with YOUR password

════════════════════════════════════════════════════════════════
STEP 2 — COPY FILES INTO YOUR ECLIPSE PROJECT
════════════════════════════════════════════════════════════════

Your project in Eclipse is named: StudentManagement_Enhanced

Copy Java files:
  FROM this ZIP:  src/main/java/com/student/...
  TO Eclipse:     StudentManagement_Enhanced/src/main/java/com/student/...

  Folder structure to paste:
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

Copy JSP files:
  FROM this ZIP:  src/main/webapp/*.jsp
  TO Eclipse:     StudentManagement_Enhanced/src/main/webapp/

  Files to paste:
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

Copy WEB-INF:
  FROM: src/main/webapp/WEB-INF/web.xml
  TO:   StudentManagement_Enhanced/src/main/webapp/WEB-INF/web.xml

Replace pom.xml:
  FROM: pom.xml (in this ZIP root)
  TO:   StudentManagement_Enhanced/pom.xml (overwrite existing)

════════════════════════════════════════════════════════════════
STEP 3 — UPDATE MAVEN IN ECLIPSE
════════════════════════════════════════════════════════════════

1. Right-click project → Maven → Update Project
2. Tick "Force Update of Snapshots/Releases"
3. Click OK
4. Wait for Eclipse to download dependencies (2-3 minutes)
5. All red errors should disappear

════════════════════════════════════════════════════════════════
STEP 4 — RUN THE PROJECT
════════════════════════════════════════════════════════════════

1. Right-click project → Run As → Run on Server
2. Select Apache Tomcat 10.1
3. Click Finish
4. Wait for console: "Server startup in [X] ms"
5. Open browser: http://localhost:8080/StudentManagement_Enhanced/home.jsp

════════════════════════════════════════════════════════════════
STEP 5 — SET UP RAZORPAY (Optional but impressive)
════════════════════════════════════════════════════════════════

1. Go to https://razorpay.com → Sign up FREE
2. Dashboard → Settings → API Keys → Generate Test Key
3. Open payFees.jsp → find this line:
   String RAZORPAY_KEY="rzp_test_YourKeyHere";
4. Replace with your key: "rzp_test_XXXXXXXXXX"

Test card for demo:
  Card Number: 4111 1111 1111 1111
  Expiry: Any future date (e.g. 12/28)
  CVV: Any 3 digits (e.g. 123)
  OTP: 1234

════════════════════════════════════════════════════════════════
STEP 6 — SET UP PYTHON AI (Optional but very impressive)
════════════════════════════════════════════════════════════════

1. Make sure Python is installed (python --version in cmd)
2. Open Command Prompt (cmd) as Administrator
3. Run these commands:

   pip install flask flask-cors

4. Navigate to python-ai folder:
   cd path\to\your\downloads\CompleteProject\python-ai

5. Start the AI server:
   python app.py

6. You should see:
   EduSphere AI API starting...
   URL: http://localhost:5000

7. Keep this cmd window OPEN during your demo
   (The AI Predict page will use it automatically)

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
WHAT TO TELL YOUR TEACHER (Copy-paste this)
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
