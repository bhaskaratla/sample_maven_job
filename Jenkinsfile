pipeline {
    agent any
    stages {
        stage('Checkout from SCM') {
            steps {
                git credentialsId: 'bhaskaratla', url: 'http://localhost:8080/gitbucket/git/bhaskar/tomcat_project.git'
            }
        }
    }
}
