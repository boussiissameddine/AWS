pipeline {
    agent any
            stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name iaas-paas --template-body file://$PWD/stack4.yaml --profile issam --region 'us-east-1'"
              }
             }
            }
            }
          
