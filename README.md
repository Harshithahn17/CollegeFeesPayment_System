# 🎓 College Fee Payment System

*Subject Name*: Advanced Java  
*Subject Code*: BCS613D  
*Name*: Harshitha H N  
*USN*: 4AL22CS058  
*Semester/Section*: VI / A

A dynamic web-based *College Fee Payment System* that allows administrators to manage student fee payments with ease. Built using *JSP, **Servlets, and **MySQL, this application follows the **MVC architecture, providing full **CRUD functionality* for student payments along with streamlined validation and user-friendly interfaces.

---

## 🚀 Features

- *CRUD Operations*:  
  - Add, Update, Delete, and Display Fee Payments  

- *Validation*:  
  - Required fields for student name, amount, and status  
  - Date validation for proper formatting  

- *MVC Pattern*:  
  - Model: JavaBeans for FeePayment  
  - View: JSP Pages  
  - Controller: Java Servlets  

- *Responsive UI*:  
  - Easy-to-use web interface using HTML/CSS  

- *MySQL Integration*:  
  - Data persistence via JDBC connection to MySQL  

---

## 📋 Prerequisites

Ensure the following tools are installed:

- JDK 8 or later  
- Apache Tomcat 9+  
- MySQL or XAMPP Server  
- MySQL Connector/J (JDBC Driver)  
- Eclipse (or any Java IDE)  
- Modern Web Browser  

---

## 🗄 Database Setup

### 1. Create the Database

sql
CREATE DATABASE IF NOT EXISTS college_fee;
USE college_fee;


### 2. Create the Table

sql
CREATE TABLE IF NOT EXISTS fee_payments (
    paymentID INT PRIMARY KEY AUTO_INCREMENT,
    studentID INT NOT NULL,
    studentName VARCHAR(100) NOT NULL,
    paymentDate DATE NOT NULL,
    amount DOUBLE NOT NULL,
    status VARCHAR(50) NOT NULL
);


### 3. Insert Sample Data

sql
INSERT INTO fee_payments (studentID, studentName, paymentDate, amount, status) VALUES
(1001, 'Harshitha H N', '2025-05-01', 25000, 'Paid'),
(1002, 'Rohit K', '2025-05-03', 27000, 'Pending');


---

## ⚙ Project Setup & Deployment

### Step 1: Create Project

- Open *Eclipse*  
- Create a *Dynamic Web Project*  
- Add folders: dao, model, servlet inside src  

### Step 2: Add JDBC Driver

- Download *MySQL Connector/J*  
- Place the .jar in WebContent/WEB-INF/lib  
- Right-click → Build Path → Add to Build Path  

### Step 3: Update DB Credentials

In FeePaymentDAO.java:

java
Connection conn = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/college_fee", 
    "root", 
    ""
);


### Step 4: Run on Tomcat

- Right-click project → *Run on Server*  
- Select Apache Tomcat 9+  
- Make sure MySQL is running  

---

## 🌐 Usage Guide

✅ *Add Payment*  
- Go to addfee.jsp  
- Fill in payment details  
- Submit to save

✅ *Update Payment*  
- Click “Edit” in feepaymentdisplay.jsp  
- Modify and submit

✅ *Delete Payment*  
- Click “Delete” to remove a record

✅ *View Payments*  
- Visit feepaymentdisplay.jsp to see all payments  

---

## 📁 Project Structure


CollegeFeePaymentSystem/
│
├── src/
│   ├── model/
│   │   └── FeePayment.java
│   ├── dao/
│   │   └── FeePaymentDAO.java
│   └── servlet/
│       ├── AddFeePaymentServlet.java
│       ├── UpdateFeePaymentServlet.java
│       └── DeleteFeePaymentServlet.java
│
├── WebContent/
│   ├── addfee.jsp
│   ├── updatefee.jsp
│   ├── feepaymentdisplay.jsp
│   └── WEB-INF/
│       └── web.xml


---

## 🎓 Learning Outcomes

- ✅ Built a working *MVC-based Java Web App*  
- ✅ Applied *JSP + Servlet + JDBC* integration  
- ✅ Practiced real-world *form handling, **database operations, and **server deployment*

---

> ✨ Developed by *Harshitha H N* | 6th Sem CSE
