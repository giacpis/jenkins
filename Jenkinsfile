pipeline {
    agent any
    stages {
        stage('retrieve-file') {
            steps {
                sh 'python --version'
            }
        }
        stage('deploy-cf') {
            steps {
                sh 'aws s3 ls'
            }
        }
    }
}
