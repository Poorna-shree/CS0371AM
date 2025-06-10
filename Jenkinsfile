pipeline {
    agent any
    tools {
        maven 'Maven' // Ensure this matches the Maven name set up in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Poorna-shree/CS0371AM.git'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Run Application') {
            steps {
                bat 'java -jar target/CS0371A-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}

