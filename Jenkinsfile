    pipeline {
        agent any
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
