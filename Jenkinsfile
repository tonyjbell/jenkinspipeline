pipeline {
    agent any
    tools {
        maven 'Local_Maven'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
                echo 'Building'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            } 
        }
    }
}