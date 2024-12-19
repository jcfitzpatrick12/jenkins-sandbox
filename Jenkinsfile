pipeline {
    agent { docker { image 'python:3.10.12' } }
    environment {
        CC = """${sh(
                returnStdout: true,
                script: 'echo "clang"'
                )}"""
    }
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
        stage('Scrap stage.') {
            steps {
                sh "printenv | grep CC"
            }
        }
    }
}


























