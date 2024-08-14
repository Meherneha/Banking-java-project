pipeline{
    agent any
    stages{
        stage('checkout the code from github'){
            steps{
                 git url: 'https://github.com/Meherneha/Banking-java-project/'
                 echo 'github url checkout'
            }
        }
        stage('codecompile with neha'){
            steps{
                echo 'starting compiling'
                sh 'mvn compile'
            }
        }
        stage('codetesting with neha'){
            steps{
                sh 'mvn test'
            }
        }
        stage('qa with neha'){
            steps{
                sh 'mvn checkstyle:checkstyle'
            }
        }
        stage('package with neha'){
            steps{
                sh 'mvn package'
            }
        }
        stage('run dockerfile'){
          steps{
               sh 'docker build -t myimg .'
           }
         }
        stage('port expose'){
            steps{


pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/Meherneha/Banking-java-project/'
                echo 'Checked out code from GitHub'
            }
        }
        stage('Compile Code') {
            steps {
                echo 'Starting compilation'
                sh 'mvn compile'
            }
        }
        stage('Test Code') {
            steps {
                sh 'mvn test'
            }
        }
        stage('QA Check') {
            steps {
                sh 'mvn checkstyle:checkstyle'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myimg .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -dt -p 8091:8091 --name c000 myimg'
            }
        }
    }
    post {
        always {
            echo 'Cleaning up...'
            sh 'docker container prune -f'
            sh 'docker image prune -f'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check logs for details.'
        }
    }
}


                
                sh 'docker run -dt -p 8091:8091 --name c000 myimg'
            }
        }   
    }
}
