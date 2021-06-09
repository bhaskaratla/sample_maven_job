pipeline {
    agent any
    stages {
        stage('Checkout from SCM') {
            steps {
                git credentialsId: 'bhaskaratla', url: 'http://localhost:8080/gitbucket/git/bhaskar/tomcat_project.git'
                     }
            }
        stage('Sonar checking') {
            steps {
                 script {
                    def scannerHome = tool 'Sonar_6.4';
                        withSonarQubeEnv("Sonar-Server") {
                        sh "${mvnHome}/bin/mvn sonar:sonar"
                        
                            }
                        }
             }
            }
        }
             }
