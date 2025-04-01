pipeline {
    agent any

    environment {
        PYTHON = 'python'  // or 'python3' if you're on Linux/macOS
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Raoajay31/mymenu.git'
            }
        }

        stage('Run Python Script') {
            steps {
                sh "${PYTHON} beescode.py"
            }
        }
    }

    post {
        success {
            echo '✅ Build and run successful!'
        }
        failure {
            echo '❌ Build failed.'
        }
    }
}
