pipeline {
        agent any
        stages {
         stage('Build') {  
              agent { docker 'maven:3-alpine' }
              steps {
               checkout scm
               sh 'mvn test'   
             }
         }   
         stage('Test') {
            agent { docker 'maven:3-alpine' }
            steps {
               checkout scm
               sh 'mvn compile'
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
