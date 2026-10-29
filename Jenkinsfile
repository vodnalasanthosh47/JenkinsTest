pipeline {
    agent any

    stages {
        stage('Check environment') {
            steps {
                sh 'python --version'
                sh 'ls -la'
            }
        }
        stage('Run') {
            steps {
                sh 'python main.py'
            }
        }
    }

    post {
        success { echo 'Build passed' }
        failure { echo 'Build failed' }
    }
}
