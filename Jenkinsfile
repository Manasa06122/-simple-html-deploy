pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-repo/your-project.git'
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
                    docker.image('html-app').run('-p 8081:80')
                }
            }
        }
    }
}
