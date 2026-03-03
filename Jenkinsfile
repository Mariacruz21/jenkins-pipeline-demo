pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker pull nginx'
            }
        }

        stage('Deploy Container') {
            steps {
                sh 'docker rm -f demo-container || true'
                sh 'docker run -d --name demo-container -p 8081:80 nginx'
            }
        }
    }
}
