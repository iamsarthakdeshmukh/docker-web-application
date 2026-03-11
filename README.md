# Dockerized Web Application 🚀

## Project Overview

This project demonstrates how to containerize a simple static website using **Docker** and deploy it using **Nginx** on a Linux server.

The application was built on an **AWS EC2 Ubuntu instance**, containerized using Docker, and the Docker image was pushed to **Docker Hub**. The project repository and documentation are maintained on GitHub.

---

## Tech Stack

* Docker
* Nginx
* AWS EC2
* Linux (Ubuntu)
* Docker Hub
* Git & GitHub

---

## Project Architecture

User Browser
↓
AWS EC2 Instance
↓
Docker Container
↓
Nginx Web Server
↓
Static HTML Website

---

## Project Structure

```
docker-web-application
│
├── Dockerfile
├── index.html
├── README.md
└── screenshots
    ├── 1-AWS Console dashboard.png
    ├── 2-EC2 instance running.png
    ├── 3-PowerShell connected to EC2.png
    ├── 4-Linux update command running.png
    ├── 5-Folder creation command.png
    ├── 6-index.html file opened in nano editor.png
    ├── 7-Dockerfile open in terminal.png
    ├── 8-Docker build process.png
    ├── 9-Docker image in list.png
    ├── 10-Running container.png
    ├── 11-Website running in browser.png
    ├── 12-Docker push successful.png
    ├── 13-GitHub repository page.png
    └── 14-Project uploaded on GitHub.png
```

---

## Implementation Steps

### 1. Launch AWS EC2 Instance

Create a Linux server using AWS EC2.

### 2. Connect to EC2

Connect to the instance using PowerShell and SSH.

### 3. Update Linux System

```
sudo apt update
```

### 4. Install Docker

```
sudo apt install docker.io -y
```

### 5. Create Project Folder

```
mkdir docker-web-app
cd docker-web-app
```

### 6. Create index.html

```
nano index.html
```

Example content:

```
<h1>Hello from Docker Container</h1>
<p>This website is running inside Docker.</p>
```

### 7. Create Dockerfile

```
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html
```

### 8. Build Docker Image

```
docker build -t docker-web-app .
```

### 9. Run Docker Container

```
docker run -d -p 80:80 docker-web-app
```

### 10. Push Image to Docker Hub

```
docker login
docker tag docker-web-app username/docker-web-app
docker push username/docker-web-app
```

### 11. Upload Project to GitHub

Push the project files and documentation to GitHub.

---

## Project Screenshots

### 1. AWS Console Dashboard

![AWS](screenshots/1-AWS%20Console%20dashboard.png)

### 2. EC2 Instance Running

![EC2](screenshots/2-EC2%20instance%20running.png)

### 3. PowerShell Connected to EC2

![PowerShell](screenshots/3-PowerShell%20connected%20to%20EC2.png)

### 4. Linux Update Command

![Linux](screenshots/4-Linux%20update%20command%20running.png)

### 5. Project Folder Creation

![Folder](screenshots/5-Folder%20creation%20command.png)

### 6. index.html File Created

![HTML](screenshots/6-index.html%20file%20opened%20in%20nano%20editor.png)

### 7. Dockerfile Created

![Dockerfile](screenshots/7-Dockerfile%20open%20in%20terminal.png)

### 8. Docker Image List

![Docker Images](screenshots/8-Docker%20image%20in%20list.png)

### 9. Docker Build Process

![Docker Build](screenshots/9-Docker%20build%20process.png)

### 10. Running Container

![Container](screenshots/10-Running%20container.png)

### 11. Website Running in Browser

![Website](screenshots/11-Website%20running%20in%20browser.png)

### 12. Docker Push Successful

![DockerHub](screenshots/12-Docker%20push%20successful.png)

### 13. GitHub Repository Page

![GitHub](screenshots/13-GitHub%20repository%20page.png)

### 14. Project Uploaded on GitHub

![Upload](screenshots/14-Project%20uploaded%20on%20GitHub.png)


---

## Key Learnings

* Containerization using Docker
* Creating Docker images with Dockerfile
* Running and managing Docker containers
* Deploying applications on AWS EC2
* Using Docker Hub for storing container images
* Managing project code using GitHub

---

## Author

Sarthak Deshmukh

GitHub: https://github.com/iamsarthakdeshmukh
