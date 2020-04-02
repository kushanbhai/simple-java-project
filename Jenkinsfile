pipeline {
     agent any
        stages {
         stage('Test') {
             agent { docker {image 'maven:3-alpine'} }
             steps {
               checkout scm
               sh 'mvn compile'
            }
         }
         stage('Deploy') {
            agent { docker {image 'maven:3-alpine'} } 
            steps {
               checkout scm
               sh 'mvn package' 
            }   
         }     
     }
 }
