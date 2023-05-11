pipeline {
    agent any
        properties([parameters([string(defaultValue: 'NULL', description: 'important', name: 'ORG_NAME', trim: false),
        string(defaultValue: 'NULL', description: 'important', name: 'ORG_ID', trim: false)
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name s3bucket --template-body file://lambdas3.json --region 'ap-south-1' --parameters ParameterKey=FunctionName,ParameterValue=${env.FunctionName} ParameterKey=EventRuleName,ParameterValue=${env.EventRuleName} ParameterKey=StackName,"
              }
             }
            }
            }
