pipeline {
    agent any
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
