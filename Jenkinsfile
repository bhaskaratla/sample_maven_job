pipeline {
    agent any
    //tools {
       // maven 'Maven'
       // docker 'Docker'
    //}
    stages {
        stage ('Checkout from SCM') {
            steps {
                git 'https://github.com/bhaskaratla/simple-java-maven-app.git'
            }
        }
    }
}
//