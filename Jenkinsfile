pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Deploy') {
            steps {
                withCredentials([aws(accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'shubham-aws-creds', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]) {
                bat "aws cloudformation create-stack --stack-name helloWorldPipeline --template-file samTemplate.json --region 'us-east-1'"
                }
            }
        }
    }
}
