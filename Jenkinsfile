pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials ('swamy-docker-hub')
        
    }
    stages {
       stage('Build') {
        steps {
            sh 'docker build -t swamy877/jenkins1 .'
        }
        }
       stage('login') {
        steps {
            sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
        }
       }
       stage('Push') {
            steps {
                sh 'docker push swamy877/jenkins1'
            }
        }
       
    }
    post {
        always {
            sh 'docker logout'
        }
    }
}