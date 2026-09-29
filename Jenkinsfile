pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                dir('Java-Docker-App') {
                    bat 'mvn clean package'
                }
            }
        }

        stage('Docker Build') {
            steps {
                dir('Java-Docker-App') {
                    bat 'docker build -t java-docker-app .'
                }
            }
        }
    }
}