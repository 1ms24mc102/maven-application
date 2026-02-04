pipeline {
    agent any

    triggers {
        cron('* * * * *')
    }

    environment {
        IMAGE_NAME = "1ms24mc102/maven-application"
        DOCKERHUB_CREDENTIALS = "dockerHub"
    }

    stages {

        stage('Checkout Source Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/1ms24mc102/maven-application.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("${IMAGE_NAME}:latest")
                }
            }
        }

        stage('Push Docker Image to Docker Hub') {
            steps {
                script {
                    docker.withRegistry('https://index.docker.io/v1/', DOCKERHUB_CREDENTIALS) {
                        dockerImage.push('latest')
                    }
                }
            }
        }
    }
}
