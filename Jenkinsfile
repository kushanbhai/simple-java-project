pipeline {
     agent { 
          docker { 
              image 'maven:3-alpine' 
              args '-v $HOME/.m2:/root/.m2' 
         }
     }
     stages {
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
