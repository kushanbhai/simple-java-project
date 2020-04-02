pipeline {
     agent any
        stages {
         stage('Build') {
             steps {
               agent {
                 docker { image 'maven:3-alpine' }
               }    
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
