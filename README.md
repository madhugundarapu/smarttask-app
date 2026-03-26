
# SmartTask Manager – DevOps Project

## Project Overview

This is a simple DevOps project where I created a basic Flask application and deployed it using Docker on AWS EC2. I also configured Nginx and CI/CD using GitHub Actions.

---

## Technologies Used

* AWS EC2 (Ubuntu)
* Python (Flask)
* Docker
* Nginx
* Git & GitHub
* GitHub Actions (CI/CD)

---

## Application

This is a simple Flask app which shows:
"SmartTask Manager Running Successfully"

---

## Steps I Followed

### 1. EC2 Setup

* Launched Ubuntu EC2 instance
* Connected using SSH
* Installed:

  * Docker
  * Git
  * Nginx
  * Python3

---

### 2. Application Setup

* Created simple Flask app (app.py)
* Installed Flask using pip
* Tested app on port 5000

---

### 3. Docker Setup

* Created Dockerfile
* Built Docker image
* Ran container on port 5000

Commands used:

```
docker build -t smarttask-app .
docker run -d -p 5000:5000 smarttask-app
```

---

### 4. Nginx Setup

* Configured Nginx as reverse proxy
* Mapped port 80 to 5000

Test:

```
curl http://localhost
```

---

### 5. GitHub Setup

* Initialized git repository
* Pushed code to GitHub

---

### 6. CI/CD Pipeline

* Used GitHub Actions
* On every push:

  * Connect to EC2
  * Pull latest code
  * Rebuild Docker image
  * Restart container

---

## Deployment Flow

GitHub → GitHub Actions → EC2 → Docker → Nginx → Browser

---

## Troubleshooting Done

* Fixed Dockerfile path issue
* Fixed port already in use error
* Fixed container name conflict
* Restarted services when needed

---

## Commands Used

Check containers:

```
docker ps
```

Stop container:

```
docker stop <container_id>
```

Remove container:

```
docker rm <container_id>
```

Docker cleanup:

```
docker system prune -a
```

---

## Output

Application is running successfully on EC2 using Docker and Nginx.

---

## Conclusion

This project helped me understand:

* Deployment process
* Docker usage
* CI/CD pipeline
* Troubleshooting issues
