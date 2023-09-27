pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from your version control system (e.g., Git)
                checkout scm
            }
        }

        stage('Build and Run Docker Compose') {
            steps {
                script {
                    // Define the Docker Compose file location (if not in the root directory)
                    def dockerComposeFile = 'docker-compose.yml'
                    
                    // Pull Docker Compose images (optional)
                    sh "docker-compose -f ${dockerComposeFile} pull"
                    
                    // Start the Docker Compose services
                    sh "docker-compose -f ${dockerComposeFile} up -d"
                }
            }
        }
    }

    post {
    }
}
