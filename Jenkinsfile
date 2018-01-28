pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                    sh 'mvn clean Package2'
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