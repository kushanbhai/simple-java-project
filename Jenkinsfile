pipeline {
    agent none    
    stages {
        stage('build') {
            agent { docker '${myimage}' }
            steps {
                checkout scm
                sh 'mvn test'
           }
        }   
    }
}    
