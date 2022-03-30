pipeline {
    agent any
    stages  {
        stage('SCM Checkout') {
            steps {
                git url: 'http://localhost:8080/gitbucket/git/bhaskar/tomcat_project.git'
            
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
