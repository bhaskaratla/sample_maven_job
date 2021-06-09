pipeline {
    agent any

    tools {
        maven 'Maven 3.5.0'
    }
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
                        sh 'mvn -X -e sonar:sonar'
                        
                            }
                        }
             }
            }
        }
             }
