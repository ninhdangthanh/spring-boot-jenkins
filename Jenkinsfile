pipeline {

    agent any
    
    stages {

        stage('Deploy Spring Boot to DEV') {
            steps {
                echo 'Deploying and cleaning'
                // sh 'docker container run -d --rm --name ninhdangthanh-springboot-jenkins -p 8081:8080 ninhdangthanh/springboot-jenkins'
                sh 'docker compose up'
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
