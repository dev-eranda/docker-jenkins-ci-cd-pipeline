pipeline {
    agent any
    environment {
        IMAGE_NAME = 'erandamadusanka/node-app'
    }
    
    stages {
        stage('SCM Checkout') {
            steps {
                retry(3) {
                    git branch: 'main', url: 'https://github.com/ErandaMadusanka/Docker-and-Jenkins-CI-CD-Pipeline'
                }
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t ${IMAGE_NAME}:${BUILD_NUMBER} .'
            }
        }
        stage('Login to Docker Hub') {
            steps {
                withCredentials([string(credentialsId: 'dockerhub-password', variable: 'DOCKER_PASSWORD')])  {
                   
                    script {
                        
                        bat """
                            echo ${DOCKER_PASSWORD} | docker login -u erandamadusanka --password-stdin
                        """
                    }
                }
            }
        }
        stage('Push Image') {
            steps {
                bat "docker push ${IMAGE_NAME}:${BUILD_NUMBER}"
            }
        }
    }
    post {
        always {
            bat 'docker logout'
        }
    }
}

