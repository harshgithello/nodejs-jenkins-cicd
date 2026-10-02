pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                bat 'npm ci'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'npm test'
            }
        }

        stage('Docker Build') {
            steps {
                echo 'Building Docker image...'
                bat 'docker build -t nodejs-jenkins-cicd:latest .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                bat 'docker rm -f nodejs-jenkins-container || exit /b 0'
                bat 'docker run -d -p 3001:3000 --name nodejs-jenkins-container nodejs-jenkins-cicd:latest'
            }
        }
    }
}