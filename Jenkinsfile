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
                bat "aws cloudformation create-stack --stack-name helloWorldPipeline --template-file samTemplate.json --region 'us-east-1'"
            }
        }
    }
}
