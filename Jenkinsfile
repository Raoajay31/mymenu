pipeline {
    agent any

    environment {
        PYTHON = 'python3'  // or 'python' if that's what your system uses
    }

    stages {
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

