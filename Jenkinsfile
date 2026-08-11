pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Build started'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing started'
                echo 'Test completed successfully'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage'
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


