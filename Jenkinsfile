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
                bat 'docker compose down'
            }
        }

        stage('Docker Compose Up') {
            steps {
             
                bat 'docker compose up -d'
            }
        }

        stage('Verificar Despliegue') {
            steps { 
                bat 'docker ps'
            }
        }
    }
}