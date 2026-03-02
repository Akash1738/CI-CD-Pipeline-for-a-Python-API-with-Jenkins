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


🧩 STEP 1: Understand the Goal

You are building:
A Flask web app
Containerized with Docker
Automatically tested and deployed using Jenkins

👉 Every time code changes, Jenkins will:

Pull the code
Run tests
Build Docker image
Deploy the app

==================================================================================================================================================================================================

🧩 STEP 2: Create the Flask Application
📄 app.py

This is the main application file.

✅ What’s happening?

Flask(__name__) creates the app

/ route returns a JSON response

0.0.0.0 allows Docker to access the app

Runs on port 5000

==================================================================================================================================================================================================

🧩 STEP 3: Add Dependencies
📄 requirements.txt

flask
pytest

✅ Why?

flask → run the web app
pytest → run automated tests in CI

=================================================================================================================================================================================================

🧩 STEP 4: Write Unit Test
📄 test_app.py

✅ Why tests?

Jenkins fails the pipeline if tests fail
Ensures code quality before deployment

=================================================================================================================================================================================================

🧩 STEP 5: Dockerize the Application
📄 Dockerfile

✅ What each line does:
Line	                      Purpose
FROM	                    Base Python image
WORKDIR	                  App directory inside container
COPY	                    Copy project files
RUN	                      Install dependencies
EXPOSE	                  App port
CMD	                      Start Flask app

=================================================================================================================================================================================================

🧩 STEP 6: Test Docker Locally

docker build -t cicd-pipeline .
docker run -d -p 5000:5000 cicd-pipeline
http://<server-ip>:5000

=================================================================================================================================================================================================

🧩 STEP 7: Push Code to GitHub

Create a repository on GitHub

Push your project:

git init
git add .
git commit -m "Initial CI/CD project"
git branch -M main
git remote add origin https://github.com/your-username/cicd-project.git
git push -u origin main

=================================================================================================================================================================================================

🧩 STEP 8: Install Jenkins & Docker on Server

On Ubuntu:

sudo apt update
sudo apt install -y docker.io
sudo apt install -y openjdk-17-jdk

Install Jenkins and start it:

sudo systemctl start jenkins
sudo systemctl enable jenkins

Allow Jenkins to use Docker:

sudo usermod -aG docker jenkins
sudo systemctl restart jenkins

==================================================================================================================================================================================================

🧩 STEP 9: Create Jenkins Pipeline
📄 Jenkinsfile

==================================================================================================================================================================================================

}
🧩 STEP 10: Run the Pipeline

Open Jenkins UI → http://<server-ip>:8080
Create Pipeline Job
Connect GitHub repo
Click Build Now

🎉 Jenkins executes all steps automatically!

==================================================================================================================================================================================================

🧩 STEP 11: Final Output

Jenkins job: ✅ SUCCESS
Docker container: ✅ RUNNING
App accessible on port 5000

==================================================================================================================================================================================================

🎯 What You Learned

✔ Flask app creation
✔ Docker containerization
✔ Jenkins pipelines
✔ CI/CD automation
✔ Real DevOps workflow

==================================================================================================================================================================================================

🚀 Next-Level Improvements

Push image to Docker Hub
Deploy on AWS EC2
Add GitHub Webhooks
Use Gunicorn + Nginx
Convert to GitHub Actions
