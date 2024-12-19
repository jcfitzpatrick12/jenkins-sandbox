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
        stage('Scrap stage.') {
            environment {
                MY_ENV = "foo"
            }
            steps {
                sh "printenv | grep foo"
            }
        }

        stage('Another scrap stage.') {
            steps {
                sh "printenv | grep foo"
            }
        }
    }
}


























