pipeline {
    agent any
    stages {
        stage('retrieve-file') {
            steps {
                sh 'rm -f /tmp/code-repo/*'
                sh 'wget https://github.com/giacpis/codecommit-fake/blob/88edee0f92b63741e02108b5e2d73136cb6960d7/stack-1/params -O /tmp/code-repo/params'
                sh 'wget https://raw.githubusercontent.com/giacpis/codecommit-fake/main/stack-1/cloudformation -O /tmp/code-repo/cloudformation'
            }
        }
        stage('deploy-cf') {
            steps {
                sh 'aws s3 ls'
                sh 'aws s3 cp /tmp/code-repo/cloudformation s3://cf-templates-tfbv34rj6yo6-eu-west-1/jenkins/cloudformation.yml'
                sh 'aws cloudformation create-stack --region eu-west-1 --stack-name Stack2 --template-url https://cf-templates-tfbv34rj6yo6-eu-west-1.s3.eu-west-1.amazonaws.com/jenkins/cloudformation.yml'
            }
        }
    }
}
