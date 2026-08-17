# 🎓 Student Management System

A web-based **Student Management System** built with **Java, JSP, Servlets, and MySQL** and automated with a complete **DevOps CI/CD pipeline** using **Jenkins, Docker, SonarQube, Terraform, Amazon ECR, Amazon EKS, and Kubernetes**.

---

## ✨ Features

* ➕ Add student records
* ✏️ Update student information
* ❌ Delete student records
* 📋 View all students in a single dashboard
* 🗄️ MySQL database integration
* 🐳 Containerized with Docker
* ☸️ Kubernetes-based deployment
* 🔄 Automated CI/CD pipeline using Jenkins

---

## 🛠️ Technology Stack

| Category                | Technology          |
| ----------------------- | ------------------- |
| Backend                 | Java, JSP, Servlets |
| Database                | MySQL               |
| Build Tool              | Maven               |
| Containerization        | Docker              |
| CI/CD                   | Jenkins             |
| Code Analysis           | SonarQube           |
| Container Registry      | Amazon ECR          |
| Infrastructure          | Terraform           |
| Container Orchestration | Kubernetes          |
| Cloud Platform          | AWS                 |

---

## 🚀 Local Deployment

### Install Java

```bash
sudo apt update
sudo apt install -y openjdk-21-jdk
java --version
```

### Install Maven

```bash
sudo apt install -y maven
mvn -version
```

### Install MySQL

```bash
sudo apt install -y mysql-server
sudo systemctl start mysql
sudo systemctl enable mysql
```

### Create the database

```bash
mysql -u root -p < sql/schema.sql
```

### Configure the database connection

Edit:

```text
src/main/resources/db.properties
```

```properties
db.url=jdbc:mysql://localhost:3306/school_db?useSSL=false&serverTimezone=UTC
db.user=root
db.password=YOUR_MYSQL_PASSWORD
```

### Build the application

```bash
mvn clean package
```

---

## 🐳 Docker Deployment

### Build the Docker image

```bash
docker build -t student-management .
```

### Run the container

```bash
docker compose up -d
```

---

## ☸️ Kubernetes Deployment

Apply the Kubernetes manifests:

```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

Check the resources:

```bash
kubectl get deployments
kubectl get services
kubectl get pods
```

---

## 🔄 CI/CD Pipeline

```text
GitHub
   │
   ▼
Jenkins
   │
   ▼
Maven Build
   │
   ▼
SonarQube Analysis
   │
   ▼
Docker Build
   │
   ▼
Amazon ECR
   │
   ▼
Terraform
   │
   ▼
Amazon EKS
   │
   ▼
Kubernetes Deployment
```

---

## 📂 Project Structure

```text
STUDENT-MANAGEMENT-APP
├── k8s
│   ├── deployment.yaml
│   └── service.yaml
├── sql
│   └── schema.sql
├── src
├── terraform
│   └── main.tf
├── Dockerfile
├── docker-compose.yaml
├── Jenkinsfile
├── Jenkinsfile-cluster
├── pom.xml
├── README.md
└── .gitignore
```

---

## 🌐 Access the Application

After deployment, open:

```text
http://YOUR_PUBLIC_IP:8080/student/students
```

---

## 🐞 Troubleshooting

| Issue                     | Solution                                    |
| ------------------------- | ------------------------------------------- |
| 404 Error                 | Verify the Tomcat deployment                |
| Database Connection Error | Check `db.properties`                       |
| Docker Build Error        | Verify the `Dockerfile`                     |
| Kubernetes Error          | Verify the deployment and service manifests |

---

## ⭐ Support

If you found this project useful, don't forget to give it a star.

Built with ❤️ using Java, AWS, Docker, Jenkins, Terraform, and Kubernetes.
