pipeline {
    //agent { docker { image 'python:3.5.1' } }
    agent any
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
        stage('mammeta') {
            steps {
                sh 'aws s3 ls'
            }
        }
    }
}
