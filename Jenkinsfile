pipeline {
    agent any

    stages {
        stage('Deploy with Docker Compose') {
            steps {
                script {
                    // Start Docker Compose services
                    sh "docker-compose up -d"
                }
            }
        }
    }

    post {
        always {
            // Clean up by stopping and removing Docker Compose services
            script {
                sh "docker-compose down"
            }
        }

    }
}
