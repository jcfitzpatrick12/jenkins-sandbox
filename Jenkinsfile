pipeline {
    agent { docker { image 'python:latest' } }
    stages {
        stage('Build') {
            steps {
                echo "Building..."
                sh 'ls -lrt'
                sh 'python3 main.py'
            }
        }
        stage('Test') {
            steps {
                echo "Testing..."
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying..."
            }
        }
    }
}


























