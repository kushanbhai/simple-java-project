pipeline {
     agent any
        stages {
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
