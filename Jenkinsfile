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
       // stage('Sonar checking') {
       //     steps {
       //          script {
       //             def scannerHome = tool 'Sonar_6.4';
       //                 withSonarQubeEnv("Sonar-Server") {
       //                 sh "${tool("Sonar1")}/ \
       //                 -Dsonar.projectKey=test-node-js \
       //                 -Dsonar.sources=. \
       //                 -Dsonar.css.node=. \
       //                 -Dsonar.host.url=http://localhost:9000 \
       //                 -Dsonar.login=your-2ccd114f601eab267de809ca08a333ec86841c84"
        //                    }
        //                }
        //     }
        //    }
        stage('Maven test') {
            steps {
                sh 'mvn test'
            }
        }
        }       
             }
