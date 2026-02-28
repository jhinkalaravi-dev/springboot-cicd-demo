pipeline {
    agent any

    stages {

        stage('Build Maven') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t jhinkalaravi/springboot-demo:latest .'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push jhinkalaravi/springboot-demo:latest'
            }
        }
    }
}