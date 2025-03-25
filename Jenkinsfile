pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo this is build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo this is test'
                
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo this deploy'
                error "pipeline failed"
            }
        }
    }

    post{
        always{
            mail to: "dhanushboga555@gmail.com",
            subject: "Test Email",
            body: "Test"
            echo "this section runs always irrespective of success or failure"
        }
        success{
            mail to: "dhanushboga555@gmail.com",
            subject: "Test Email success",
            body: "Test success"
            echo "this section runs only if pipeline success"
        }
        failure{
            mail to: "dhanushboga555@gmail.com",
            subject: "Test Email failure",
            body: "Test failure"
            echo "this section runs only if pipeline failure"
        }
    }
}