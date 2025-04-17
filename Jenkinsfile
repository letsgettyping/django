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
                    sh 'docker build -t django_demo .'

                }
            }
        }

        stage('Run Django in Docker') {
            steps {
                script {
                    sh 'docker run -d -p 8000:8000 django_demo'
                }
            }
        }
    }
}