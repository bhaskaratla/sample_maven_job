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
                    def scannerHome = tool 'Sonar1';
                        withSonarQubeEnv("Sonar1") {
                        sh "${tool("Sonar1")}/bin/sonar-scanner \
                        -Dsonar.projectKey=test-node-js \
                        -Dsonar.sources=. \
                        -Dsonar.css.node=. \
                        -Dsonar.host.url=http://localhost:9000 \
                        -Dsonar.login=your-2ccd114f601eab267de809ca08a333ec86841c84"
                            }
                        }
             }
            }
        }
             }
