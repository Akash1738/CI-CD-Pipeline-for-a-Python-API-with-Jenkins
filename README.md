🚀 CI/CD Pipeline for Flask Application (Docker + Jenkins)

This project demonstrates a complete CI/CD pipeline for a simple Flask REST API, using Docker for containerization and Jenkins for continuous integration and deployment.

================================================================================================================================================================================================

📌 Project Overview

The pipeline automatically:
Pulls source code from GitHub
Installs dependencies
Runs unit tests
Builds a Docker image
Deploys the application in a Docker container
This project is ideal for DevOps beginners and CI/CD learning.

================================================================================================================================================================================================

🐳 Docker Instructions

Docker build Image
docker build -t cicd-pipeline .

Docker run Container
docker run -d -p 5000:5000 cicd-pipeline

=================================================================================================================================================================================================

🔁 Jenkins CI/CD Pipeline

The Jenkinsfile defines the following stages:
Checkout Code
Install Dependencies
Run Tests
Build Docker Image
Deploy Application

=================================================================================================================================================================================================

▶️ How to Run Jenkins Pipeline

Install Jenkins on your server
Install Docker on the Jenkins machine
Create a new Pipeline Job
Connect your GitHub repository
Run the pipeline

=================================================================================================================================================================================================

📝 Sample Resume Description

Built an end-to-end CI/CD pipeline using Jenkins and Docker to automate testing, containerization, and deployment of a Flask-based REST API.

=================================================================================================================================================================================================
