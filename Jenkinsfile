stage('Run Docker Container') {
    steps {
        sh '''
        docker rm -f practice-container || true
        docker run -d -p 8082:80 --name practice-container practice-app
        '''
    }
}
