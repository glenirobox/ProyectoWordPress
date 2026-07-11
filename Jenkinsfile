pipeline {
    agent any

    stages {
        stage('Verificar Docker') {
            steps {
                sh 'docker --version'
            }
        }

        stage('Detener Contenedores') {
            steps {
                // Pon aquí tu comando con sh si usas docker-compose down, ej:
                sh 'docker compose down' 
            }
        }

        stage('Levantar Contenedores') {
            steps {
                // Pon aquí tu comando con sh si usas docker-compose up, ej:
                sh 'docker compose up -d'
            }
        }

        stage('Verificar Servicios') {
            steps {
                sh 'docker ps'
            }
        }
    }
}