pipeline {
    agent any
    
    stages {
        /*stage('Build') {
            steps {
              //  sh 'gulp build' // Assuming you're using Gulp for your HTML project
            }
        }
        
        stage('Test') {
            steps {
              //  sh 'npm test' // Execute your HTML/CSS/JavaScript tests here
            }
        }
        */
        stage('Deploy') {
            steps {
                // Example deployment script using rsync
                script {
                    // Copy files to remote server using rsync
                    sh '''
                    rsync -avz -e "ssh -i 192.168.254.29" S:\devops ubuntu@52.91.221.228:/path/to/destination/directory
                    '''
                }
            }
        }
    }
}
