pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Sahi-thi-3377/lab3.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                echo "Installing testing framework..."
                bat 'pip install pytest'
            }
        }
        stage('Run Unit Tests') {
            steps {
                echo "=========================================="
                echo "Build Number: ${env.BUILD_NUMBER}"
                echo "Job Name: ${env.JOB_NAME}"
                echo "Workspace: ${env.WORKSPACE}"
                echo "=========================================="
                
                echo "Executing unit tests in verbose mode..."
            }
        }
    }
}
