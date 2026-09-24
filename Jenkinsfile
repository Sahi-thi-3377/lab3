pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install --upgrade pip
                    pip install pytest
                '''
            }
        }
        stage('Run Unit Tests (verbose)') {
            steps {
                sh '''
                    . venv/bin/activate
                    pytest -v test_app.py
                '''
            }
        }
    }
}
