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
