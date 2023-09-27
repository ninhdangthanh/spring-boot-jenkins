pipeline {

    agent any
    

    stages {
        stage('Build and Run Docker Compose') {
            steps {
                sh "docker-compose up -d"
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
