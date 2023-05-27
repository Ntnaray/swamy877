node { checkout scm
    environment {
        DOCKERHUB_CREDENTIALS = credentials ('swamy-docker-hub')
 
    }
    stage('Build and Push') {
        docker.withRegistry('', 'swamy-docker-hub')
        {
            def CustomImage = docker.build('swamy877/jenkins-dockerimage')
            CustomImage.push()
        }
    
    } 
}