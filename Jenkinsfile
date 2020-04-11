pipeline {
    agent {
        docker {
            image '${myimage}'
        }
    }
    stages {
        stage('build') {
            steps {
                checkout scm
                sh 'mvn test'
            }
        }  
        stage('Test') {
             steps {
                 checkout scm
                 sh 'mvn compile'
            }
         }
         stage('Deploy') {
             steps {
                 checkout scm
                 sh 'mvn package'
             }
         }    
    }
}    
