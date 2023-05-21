pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
            sh "echo ${env.workspace}"
            sh "./whileloop.sh"
            }
        }
        }
    }
