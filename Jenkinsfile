pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/chintudinesh/devopsjenkins.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'docker build -t my-web-app .'
            }
        }
        
        stage('Test') {
            steps {
                // Add your test commands here
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8080:80 my-web-app'
            }
        }
    }
}
