
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Fetching source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building EventProject'
                bat 'if exist index.html (echo Build Successful) else (exit /b 1)'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing EventProject'
                bat 'if exist index.html (echo Test Passed) else (exit /b 1)'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage completed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
