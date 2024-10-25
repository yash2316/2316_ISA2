pipeline {
    agent any

  node {
    checkout scm
}

    stages {

        stage('Build Docker Image') {
            steps {
                script {
                    bat "docker build -t 2316 ."
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    bat "docker run -d --name 2316 2316"
                }
            }
        }
    }
}
