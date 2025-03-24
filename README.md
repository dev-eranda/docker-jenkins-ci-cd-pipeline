# CI/CD Pipeline with Docker and Jenkins

**Developed By:** Eranda Samarasinghe
<hr />

## Project Backgroud and Overview
This repository contains code for setting up a Continuous Integration/Continuous Deployment (CI/CD) pipeline using Docker and Jenkins. The pipeline automates the process of building, testing, and deploying applications, ensuring efficiency and consistency in software development workflows
<hr />

## Technical Details
Core technologies used: 

- **Docker, Jenkins**
<hr />

## Requirements
- GitHub account
- Jenkins server
- DockerHub account
- Docker installed on Jenkins server
  
## Installation
1. Clone repository:
   ```sh
   git clone https://github.com/dev-eranda/docker-jenkins-ci-cd-pipeline.git
   
2. Set up Jenkins on your server and configure it to monitor the GitHub repository for changes.
3. Ensure you have an account on DockerHub where Jenkins can push Docker images. 
4. In Jenkins, create a new pipeline job and configure it to use the provided Jenkinsfile in this repository.
5. Trigger a build manually or make a code change in the repository to initiate the CI/CD pipeline.
   

