pipeline {
    agent any
    
    stages {
        stage('reset workspace'){
            steps {
                sh 'sudo rm -rf * | echo `pwd`'
            }
        }
        stage('Git clone') {
            steps {
              sh 'sudo git clone https://github.com/Majid-khan191/jenkins_Docker-project.git'
            }
        }
        stage('Initialize'){
            steps{
                sh 'sudo npm init --yes'
            }
        }
        stage('Build App'){
            steps{
                sh 'sudo npm install express --save'
            }
        }
        stage('Deploy App'){
            steps{
                sh "sudo cp ./Jenkins_Docker-project/docker-compose.yml . | sudo cp ./Jenkins_Docker-project/Dockerfile . | sudo cp ./Jenkins_Docker-project/server.js . "
                sh "sudo docker-compose up -d"
            }
        }
    }
}
