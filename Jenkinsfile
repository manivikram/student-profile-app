pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Code checked out from GitHub via SCM'
            }
        }
        stage('Verify') {
            steps {
                sh 'ls -la'
                sh 'date'
            }
        }
        stage('Info') {
            steps {
                echo "Build number: ${BUILD_NUMBER}"
                echo "Job name: ${JOB_NAME}"
            }
        }
    }
}
