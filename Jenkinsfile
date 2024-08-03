pipeline {
    agent any
    tools {
        maven 'Maven'  // The name you provided during Maven configuration
    }
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/mohamed10945/jenkins.git' , branch : 'main'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
