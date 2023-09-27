pipeline {

    agent any
    

    stage('Build and Run Docker Compose') {
        steps {
            script {
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
