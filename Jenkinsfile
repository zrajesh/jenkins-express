pipeline {
    agent any
    stages {
        stage("checkout") {
            steps{
                checkout scm
            }
        }
        stage("Test") {
            steps{
                sh 'sudo apt-get update'
                sh 'sudo apt install npm'
                sh 'npm install'
                sh 'npm test'
            }
        }

        stage("Build") {
            steps{
                sh 'npm run build'
            }
        }
    }
}