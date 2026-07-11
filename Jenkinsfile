pipeline {
    agent any

    stages {
        stage('Checkout desde Git') {
            steps {
                // Descarga el código automáticamente de GitHub
                checkout scm
            }
        }

        stage('Docker Compose Down') {
            steps {
                // Apaga servicios previos para limpiar el ambiente en Linux
                sh 'docker compose down'
            }
        }

        stage('Docker Compose Up') {
            steps {
                // Levanta WordPress y MySQL en segundo plano en Linux
                sh 'docker compose up -d'
            }
        }

        stage('Verificar Despliegue') {
            steps {
                // Muestra los contenedores activos en la consola de Jenkins
                sh 'docker ps'
            }
        }
    }
}