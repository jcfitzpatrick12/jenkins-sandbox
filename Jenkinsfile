pipeline {
    agent { docker { image 'python:3.10.12' } }

    environment {
        MY_ENV = "foo"
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


























