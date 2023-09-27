pipeline {

    agent any
    

    stage('Build and Run Docker Compose') {
        steps {
            script {
                // Define the Docker Compose file location (if not in the root directory)
                def dockerComposeFile = 'docker-compose.yml'
                
                // Start the Docker Compose services
                sh "docker-compose -f ${dockerComposeFile} up -d"
            }
        }
    }


    post {
        // Clean after build
        always {
            cleanWs()
        }
    }
}
