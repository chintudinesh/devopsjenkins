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
        stage('Build') {
            steps {
                sh 'mvn --version'
                sh 'ls -lrt'
                sh 'ls -l'
                sh 'ls -l target'
                sh 'cd /var/lib/jenkins/workspace/ewebsite'
                ls '-lrt'
                //sh 'mvn clean package'
                
                
            }
        }
        stage('Test') {
          steps {
              sh 'mvn test'
           }
       }
       /* stage('Deploy') {
          steps {
                //sh scp -i devops-key.pem your-artifact.jar ubuntu@your-ec2-instance:/path/to/destination
            sh 'scp -i devops_key.pem your-artifact.jar ubuntu@52.91.221.228:/home/ubuntu'
                //sh ssh -i devops-key.pem ubuntu@52.91.221.228 'java -jar /path/to/your-artifact.jar'
          sh 'ssh -i devops_key.pem ubuntu@52.91.221.228 'java -jar /home/ubuntu/your-artifact.jar''
          }
        }*/
    }
}
