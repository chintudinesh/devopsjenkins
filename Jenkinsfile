pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from Git
                git 'https://github.com/chintudinesh/web.git'
            }
        }
        stage('Build') {
            steps {
                // Build your website (e.g., compile assets, generate static files)
                sh 'npm install' // Assuming your website uses npm
                sh 'npm run build' // Assuming your website uses npm scripts for building
            }
        }
        stage('Deploy') {
            steps {
                // Deploy your website (e.g., copy files to server)
                // Replace 'server_address' and 'destination_folder' with your actual server details
                sh 'scp -r * user@52.91.221.228:webapplication'
            }
        }
    }

    post {
        success {
            // If the pipeline completes successfully, print a success message
            echo 'Website deployed successfully!'
        }
        failure {
            // If the pipeline fails, print an error message
            echo 'Failed to deploy website!'
        }
    }
}
