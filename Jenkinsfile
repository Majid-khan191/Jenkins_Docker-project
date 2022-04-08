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
              sh 'sudo git clone https://github.com/Armaan-zaheer/pipeline-jenkins.git'
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
                sh "sudo cp ./pipeline-jenkins/docker-compose.yml . | sudo cp ./pipeline-jenkins/Dockerfile . | sudo cp ./pipeline-jenkins/server.js . "
                sh "sudo docker-compose up -d"
            }
        }
    }
}
