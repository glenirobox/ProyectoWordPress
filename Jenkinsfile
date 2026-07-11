pipeline {
    agent any

    stages {

        stage('Verificar Docker') {
            steps {
                powershell 'docker ps'
            }
        }

        stage('Detener Contenedores') {
            steps {
                powershell 'docker compose down'
            }
        }

        stage('Levantar Contenedores') {
            steps {
                powershell 'docker compose up -d'
            }
        }

        stage('Verificar Servicios') {
            steps {
                powershell 'docker compose ps'
            }
        }
    }
}