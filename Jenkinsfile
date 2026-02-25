stage('Run Docker Container') {
    steps {
        sh '''
        docker ps -a
        docker stop practice-container || true
        docker rm practice-container || true
        docker run -d -p 8082:80 --name practice-container practice-app
        '''
    }
}
