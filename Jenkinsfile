pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code already checked out by Jenkins SCM step'
            }
        }

        stage('Verify Files') {
            steps {
                sh 'ls -la'
                sh 'test -f index.html && echo "index.html found"'
            }
        }

        stage('Check Content') {
            steps {
                sh 'grep -o "Student Details\\|Contact Information\\|Welcome to the" index.html'
            }
        }

        stage('Report') {
            steps {
                echo "Build number: ${BUILD_NUMBER}"
                sh 'wc -l index.html'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline completed successfully'
        }
        failure {
            echo '❌ Pipeline failed — check console output'
        }
    }
}
