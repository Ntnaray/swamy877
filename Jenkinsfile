pipeline {
    agent any
    stages{
        stage("Build"){
            sh "echo ${env.workspace}"
            sh "./whileloop.sh"
        }
    }
}