pipeline {
    agent any
        stages {
            stage('Build') {
                agent docker { { image 'maven:3-alpine' } }
                steps {
                    checkout scm
                    sh 'mvn test'
               }
          }
      }
 }
