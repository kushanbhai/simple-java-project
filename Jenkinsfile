pipeline {
     agent any
     stages {
          agent { docker 'maven:3-alpine' }
          stage('Build') {
             steps {
                 checkout scm
                 sh 'mvn test'
           }
         }
         stage('Test') {
             agent any
             steps {
                 checkout scm
                 sh 'mvn compile'
             }
         }
         stage('Deploy') {
             agent any
             steps {
                 checkout scm
                 sh 'mvn package'
             }
         }  
      }
  }

