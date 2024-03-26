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
               
            }
        }
        
       
        
        stage('Deploy') {
            steps {
                sh 'cp -r ./* /path/to/your/webserver/root'
            }
        }
    }
}
