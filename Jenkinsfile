pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Specify the main branch explicitly
                git branch: 'main', url: 'https://github.com/Manasa06122/-simple-html-deploy.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('html-app')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('html-app').run('-p 8082:80')
                }
            }
        }
    }
}
