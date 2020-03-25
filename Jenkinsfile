pipeline {
     agent any
     stages {
          stage('Build') {
             agent { $docker }     
             steps {
                 checkout scm
                 sh 'mvn test'
           }
         }
         stage('Test') {
              agent { $docker }  
             steps {
                 checkout scm
                 sh 'mvn compile'
             }
         }
         stage('Deploy') {
              agent { $docker }  
             steps {
                 checkout scm
                 sh 'mvn package'
             }
         }  
      }
  }

