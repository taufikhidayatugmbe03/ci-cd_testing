pipeline {
    agent any
    environment {
        DOCKER_CREDENTIALS = credentials('docker-hub')
    }
    stages {
        stage('BUILD') {
            steps {
                sh 'docker build -t taufik2311/alpine:latest .'
            }
        }
        stage('LOGIN') {
            steps {
                sh 'echo $DOCKERHUB_CREDENTIAL_PSW | docker login -u $DOCKERHUB_CREDENTIAL_USR --password-stdin'
            }
        }
        stage(PUSH) {
            steps {
                sh 'docker push taufik2311/alpine:latest'
            }
        }
    }
    post {
        alsways {
            sh 'docker logout'
        }
    }
}
