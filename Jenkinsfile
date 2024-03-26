pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout([$class: 'GitSCM', 
                        branches: [[name: 'main']],
                        userRemoteConfigs: [[url:'https://github.com/chintudinesh/devopsjenkins.git',
                                             credentialsId: 'github-token']]])
                }
            }
        }
        // Add additional stages as needed
    }
}
