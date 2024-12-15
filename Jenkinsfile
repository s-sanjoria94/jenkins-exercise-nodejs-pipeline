pipeline {
    agent { label 'linux' }
    stages {
        stage('SCM'){
            steps {
                git branch: 'main', url: 'https://github.com/bobbybabu007/jenkins-exercise-nodejs-pipeline.git'
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
        stage('Run Tests in Parallel') {
            failFast true
            parallel {
                stage('Unit Test 1') {
                    steps {
                        echo "Unit Test 1 executing"
                        sleep 10
                    }
                }
                stage('Unit Test 2') {
                    steps {
                        echo "Unit Test 2 executing"
                        sleep 10
                    }
                }
                stage('Unit Test 3') {
                    steps {
                        echo "Unit Test 3 executing"
                        sleep 10
                    }                    
                }
            }
        }
        stage('Sonarqube Scan') {
            steps {
                echo 'Sonar scan works'
            }
        }    
        stage('Deliver Package') {
            steps {
                echo 'Delivering to Artifactory'
            }
        } 
    
    }
}
