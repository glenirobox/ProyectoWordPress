pipeline {
    agent any

    stages {
        stage('Checkout desde Git') {
            steps {
                checkout scm
            }
        }

        stage('Docker Compose Down') {
            steps {
                sh 'docker compose down'
            }
        }

        stage('Docker Compose Up') {
            steps {
                sh 'docker compose up -d'
            }
        }

        stage('Verificar Despliegue') {
            steps {
                sh 'docker ps'
            }
        }
    }
}