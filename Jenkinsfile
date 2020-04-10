pipeline {
    agent none
        stages {
            stage('Build') {
                agent { docker '${myimage}' }
                steps {
                    checkout scm
                    sh 'mvn test'
               }
          }
      }
 }
