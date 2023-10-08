pipeline {
    agent any

    stages {
        stage('Deploy with Docker Compose') {
            steps {
                sh "java --version"
                sh "ls -l"
                sh "docker compose up"
            }
        }
    }

    post {
        always {
            // Clean up by stopping and removing Docker Compose services
            script {
                sh "docker-compose  down"
            }
        }

    }
}
