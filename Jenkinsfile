pipeline {
    agent any

    stages {
        stage('Install Python') {
            steps {
                sh '''
                    apt-get update
                    apt-get install -y python3 python3-venv python3-pip
                    python3 --version
                '''
            }
        }

        stage('Verify Installation') {
            steps {
                sh 'which python3'
                sh 'python3 -m pip --version'
            }
        }
    }

    post {
        success {
            echo '✅ Python installed successfully via Jenkinsfile'
        }
        failure {
            echo '❌ Installation failed — check console output'
        }
    }
}
