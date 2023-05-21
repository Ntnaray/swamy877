pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
            sh "echo ${env.workspace}"
            sh "ls -ltr"
            sh "./whileloop.sh"
            }
        }
        }
    }
