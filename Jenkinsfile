pipeline {
    agent any
    stages {
        stage('retrieve-file') {
            steps {
                sh 'cd /tmp/code-repo'
                sh 'rm -f *'
                sh 'wget https://github.com/giacpis/codecommit-fake.git/stack-1/params'
            }
        }
        stage('deploy-cf') {
            steps {
                sh 'aws s3 ls'
            }
        }
    }
}
