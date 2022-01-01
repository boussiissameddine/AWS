def commit_id
pipeline {
    agent any
    stages {
        stage('preparation') {
            steps {
                checkout scm
                sh "git rev-parse --short HEAD > .git/commit-id"
                script {
                    commit_id = readFile('.git/commit-id').trim()
                }
            }
        }
        stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name iaas-paas --template-body file://$PWD/stack4.yaml --profile issam --region us-east-1"
              }
             }
            }
    }
}
