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

                sh '''
                    echo "Jenkins Build Successful" > build-info.txt
                    echo "Build Number: ${BUILD_NUMBER}" >> build-info.txt
                    echo "Build Date: $(date)" >> build-info.txt
                '''

                sh 'cat build-info.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing started'
                echo 'Test completed successfully'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
            archiveArtifacts artifacts: 'build-info.txt', fingerprint: true
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
