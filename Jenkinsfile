pipeline {
    agent any
    stages {
        stage('build') {
            agent { 
                docker {
                    image '${myimage}'
                }
            }
            steps {
                checkout scm
                 sh 'mvn test'
           }
        }  
    }
}    
