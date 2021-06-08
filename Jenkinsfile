pipeline {
    agent any
    stages {
        stage('Checkout from SCM') {
            steps {
                git credentialsId: 'bhaskaratla', url: 'http://localhost:8080/gitbucket/git/bhaskar/tomcat_project.git'
            }
        stage('Sonar checking') {
            steps {
                 script {
                    def scannerHome = tool 'Sonar';
                        withSonarQubeEnv("sonarqube-container") {
                        sh "${tool("sonarqube")}/bin/sonar-scanner \
                        -Dsonar.projectKey=test-node-js \
                        -Dsonar.sources=. \
                        -Dsonar.css.node=. \
                        -Dsonar.host.url=http://localhost:9000 \
                        -Dsonar.login=your-generated-token-from-sonarqube-container"
                            }
                        }
             }
            }
        }
    }
}
