pipeline {
    agent any 
        stages {
            stage('Build') {
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
