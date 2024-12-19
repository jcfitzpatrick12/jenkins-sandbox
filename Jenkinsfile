pipeline {
    agent { docker { image 'python:3.10.12' } }
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


























