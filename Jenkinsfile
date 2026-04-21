pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Hasini061/CI-NODE-App.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run Application') {
            steps {
               bat 'node app.js'
            }
        }
         stage('Run Tests') {
            steps {
               bat 'node test'
            }
        }
    }
    post {
        success {
            echo 'CI Pipeline Success'
        }
        failure{
            echo 'CI Pipeline Failure'
        }
    }
}