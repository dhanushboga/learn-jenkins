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
                // error "pipeline failed"
            }
        }
    }

    post{
        always{
            
            echo "this section runs always irrespective of success or failure"
        }
        success{
        
            echo "this section runs only if pipeline success"
        }
        failure{
           
            echo "this section runs only if pipeline failure"
        }
    }
}