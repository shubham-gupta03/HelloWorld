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
                sh "aws cloudformation create-stack --stack-name helloWorldPipeline --template-body file://simplests3cft.json --region 'us-east-1'"
            }
        }
    }
}
