pipeline {
    agent { docker { image 'maven:3-alpine' } }
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
