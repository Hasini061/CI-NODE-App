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
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t ci-node-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 3000:3000 --name ci-container ci-node-app'
            }
         }
        }
    }
}

