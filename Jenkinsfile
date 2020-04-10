pipeline {
    agent {
        docker {
            image '${myimage}'
        }
    }
    stages {
        stage('Build') {
            steps {
               checkout scm
               sh 'mvn test'
             }
         }
    }
}
