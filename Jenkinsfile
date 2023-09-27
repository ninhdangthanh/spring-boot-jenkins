pipeline {
    agent any

    stages {
        stage('Deploy with Docker Compose') {
            steps {
                sh "docker-compose up -d"
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
