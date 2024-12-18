pipeline {
    agent { label 'linux' }
    stages {
        stage('SCM'){
            steps {
                git branch: 'main', url: 'https://github.com/s-sanjoria94/jenkins-exercise-nodejs-pipeline.git'
            }
        }
        stage('Build') { 
            steps {
                sh 'printenv' 
                sh 'pwd'
                sh 'whoami'
                echo '$PATH'
                sh 'which npm'
                sh 'ls -al'
                sh 'nodejs -v'
                sh 'npm -v'
                sh 'npm install'    
            }
        }
    } 
} 

