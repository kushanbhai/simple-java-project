pipeline {
    agent none    
    stages {
        stage('build') {
            agent { docker 'openjdk:7' }
            steps {
                sh 'java -version'
           }
        }   
    }
}    
