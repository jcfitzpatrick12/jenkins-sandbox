pipeline {
    agent { docker { image 'python:3.10.12' } }
    environment {
        MY_CREDS = credentials('jimmy-secret-credentials')
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
            parameters {
                string(name: 'STATEMENT', defaultValue: 'hello; ls /', description: 'What should I say?')
            }
            steps {
                echo "echo ${STATEMENT}"
            }
        }
    }
}


























