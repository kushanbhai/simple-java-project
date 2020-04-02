pipeline {
     agent any
        stages {
          stage('Compile') {
             agent { docker 'maven:3-alpine' }
             steps {
               checkout scm 
               sh 'mvn compile'
             }
          }   
          stage('Test') {
             agent { docker 'maven:3-alpine' }
             steps {
               checkout scm
               sh 'mvn test'
             }
          }
         stage('Deploy') {
            agent { docker 'maven:3-alpine' } 
            steps {
               checkout scm
               sh 'mvn package' 
            }   
         }     
     }
 }
