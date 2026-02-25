pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git 'https://github.com/jatin-sharma9/devops-project-1.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t practice-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker stop practice-container || true
                docker rm practice-container || true
                docker run -d -p 8082:80 --name practice-container practice-app
                '''
            }
        }
    }
}
