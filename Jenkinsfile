pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo 'Cloning repo...'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('django_demo')
                }
            }
        }

        stage('Run Django in Docker') {
            steps {
                script {
                    docker.image('django_demo').run('-p 8000:8000')
                }
            }
        }
    }
}