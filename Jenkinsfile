pipeline {
    agent { docker { image 'python:3.10.12' } }
    stages {
        stage('Build') {
            steps {
                echo "Building..."
                sh """
                    python3 -m venv ./venv && \
                    . ./venv/bin/activate && \
                    pip install . && \
                    say-hello
                    """
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


























