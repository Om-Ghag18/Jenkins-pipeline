# Jenkins CI/CD Pipeline Project

This repository contains a **Jenkins CI/CD pipeline project**. It demonstrates how to automate build, test, and deployment of a Maven-based Java application using Jenkins.

---

## Project Overview

The goal of this project is to implement a **fully automated CI/CD pipeline** using Jenkins that:

- Builds a Maven Java project
- Runs unit tests
- Performs static code analysis (optional)
- Deploys the application automatically on success

This pipeline ensures **faster, reliable, and consistent deployments** with minimal manual intervention.

---

## Project Structure

maven-app/
│
├── Jenkinsfile-CI # Jenkins pipeline configuration for Continuous Integration
├── jenkinsfile-CD # Jenkins pipeline configuration for Continuous Deployment
├── pom.xml # Maven project configuration
├── settings.xml # Maven settings
├── src/
│ ├── main/java/com/example/laundry/LaundryService.java
│ └── test/java/com/example/laundry/LaundryServiceTest.java
└── README.md # Project documentation



---

## Key Technologies Used

- **Jenkins** – for CI/CD pipeline automation  
- **Maven** – build and dependency management  
- **Java** – application code  
- **Git/GitHub** – source code management  
- **Linux/Windows** – environment for Jenkins agents  

---

## CI/CD Pipeline Workflow

1. **Commit Code:** Push code changes to GitHub.  
2. **Jenkins Trigger:** Jenkins detects the commit and triggers the pipeline.  
3. **Build Stage:** Maven compiles the application.  
4. **Test Stage:** Unit tests are executed to ensure code quality.  
5. **Deploy Stage:** On successful build and tests, the application is deployed to the configured environment.  

---

## How to Use

1. Clone this repository:
```bash
git clone git@github.com:Om-Ghag18/Jenkins-pipeline.git



Open Jenkins and create a new pipeline.

Configure the pipeline to use the Jenkinsfile-CI or jenkinsfile-CD in this repository.

Trigger the pipeline manually or automatically on code commits.

Benefits

Automates build, test, and deployment process

Reduces manual errors

Faster delivery of features and fixes

Provides visibility of build and deployment status
