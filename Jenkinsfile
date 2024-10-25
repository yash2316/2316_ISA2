pipeline {
    agent any

    stages {

        stage('clone github repo') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    bat "docker build -t 2316 ."
                }
            }
        }


        stage('Delete container named 2316') {
            steps {
                script {
                    bat "docker rm --force 2316"
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
