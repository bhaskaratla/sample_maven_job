pipeline {
    agent any
    stages  {
        stage('SCM Checkout') {
            steps {
                git url: 'https://github.com/bhaskaratla/sample_maven_job.git'
            
            }
        }
        stage('1st stage') {
            steps {
                sh 'echo "Hello world"'
                }
        }
        stage('2nd stage'){
            steps {
                sh 'echo "Hello World 2nd time :-)"'
                }
        }
    }
}
