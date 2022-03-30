pipeline {

    agent any
    tools {
	maven 'Maven 3.5.0'
    }
    stages  {
        stage('SCM Checkout') {
            steps {
                git url: 'https://github.com/bhaskaratla/sample_maven_job.git'
            
            }
        }
        stage('Maven Test') {
            steps {
                sh 'mvn test'
                }
        }
        stage('Compile and Validate'){
            steps {
                sh 'mvn compile'
		sh 'mvn validate'
                }
        }
    }
}
