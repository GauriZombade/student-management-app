# 🎓 Student Management System

> A modern web-based application for managing student records efficiently using **Java, MySQL, Maven, and Apache Tomcat**.

---

## ✨ Features

* ➕ Add new student records
* ✏️ Update student information
* ❌ Delete existing records
* 📋 View all students in a centralized dashboard
* 🗄️ MySQL database integration
* ⚡ Fast and lightweight application

---

## 🛠️ Tech Stack

* **Backend:** Java (Servlets & JSP)
* **Build Tool:** Maven
* **Database:** MySQL
* **Application Server:** Apache Tomcat
* **Version Control:** Git & GitHub

---

## 📋 Prerequisites

Install the following dependencies before running the application.

### Java JDK 21

```bash
sudo apt update
sudo apt install -y openjdk-21-jdk
java --version
```

### Maven

```bash
sudo apt install -y maven
mvn -version
```

### MySQL Server

```bash
sudo apt install -y mysql-server
sudo systemctl start mysql
sudo systemctl enable mysql
```

### Apache Tomcat

Download and install **Apache Tomcat 10 or 11**.

---

## 🚀 Installation

### 1. Clone the repository

```bash
git clone <repository-url>
cd student-management-system
```

### 2. Create the database

```bash
mysql -u root -p < sql/schema.sql
```

This command creates the `school_db` database and the `students` table.

### 3. Configure the database connection

Edit the `src/main/resources/db.properties` file.

```properties
db.url=jdbc:mysql://localhost:3306/school_db?useSSL=false&serverTimezone=UTC
db.user=root
db.password=YOUR_MYSQL_PASSWORD
```

### 4. Build the project

```bash
mvn clean package
```

The generated WAR file will be available at:

```text
target/student-management.war
```

### 5. Deploy the application

```bash
sudo cp target/student-management.war /opt/tomcat/webapps/student.war
sudo /opt/tomcat/bin/startup.sh
```

### 6. Access the application

```text
http://YOUR_PUBLIC_IP:8080/student/students
```

---

## 📂 Project Structure

```text
student-management-system
├── src
├── sql
├── images
├── pom.xml
└── README.md
```

---

## 🐞 Troubleshooting

| Issue                 | Solution                                       |
| --------------------- | ---------------------------------------------- |
| 404 Error             | Verify the Tomcat deployment directory.        |
| MySQL Driver Error    | Run `mvn dependency:tree`.                     |
| Database Access Error | Check `db.properties` and rebuild the project. |

---

## 🤝 Contributing

Contributions are welcome. Feel free to fork the repository and submit a pull request.

---

## ⭐ If you like this project, don't forget to star the repository!
