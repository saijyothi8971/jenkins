pipeline {
    agent any
    parameters{
        string(defaultValue: 'NULL', description: 'important', name: 'stack-name', trim: false)
        }       
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack $stack-name --template-body file://lambdas3.json --region 'ap-south-1' --parameters ParameterKey=FunctionName,ParameterValue=${env.FunctionName} ParameterKey=EventRuleName,ParameterValue=${env.EventRuleName} ParameterKey=StackName,"
              }
             }
            }
            }
