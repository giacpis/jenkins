pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
        stage('mammeta') {
            steps {
                sh 'aws s3 list'
            }
        }
    }
}
