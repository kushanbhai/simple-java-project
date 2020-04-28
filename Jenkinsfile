pipeline {
     agent none
     stages {
         stage('Build') {
             agent any
             steps {
                 checkout scm
                 sh 'mvn test'
            }
        }
    }
}
