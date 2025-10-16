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

## Purpose
The Continuous Deployment (CD) pipeline automates the deployment of the Java application JAR from Nexus to a remote EC2 server.

## Pipeline Overview
Source: Nexus Repository (maven-releases)
Target: EC2 Server (13.204.79.114)
Process: Connects to EC2, installs Java if needed, downloads the JAR, and runs the application.

## Stages
-Test SSH Connection: Verifies the SSH connection to the EC2 server.
-Installing Java & checking version: Ensures openjdk-17-jdk is installed on the EC2 server before proceeding.
-Downloading JAR: Downloads the LaundryApp-1.1.4.jar from the Nexus repository.
-Sending files over scp: Copies the downloaded JAR file to the home directory of the ubuntu user on the EC2 server
-Running Java jar: Executes the Java application on the remote server.
