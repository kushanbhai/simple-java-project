pipeline {
     agent none
     stages {
         stage('first') {
             agent any 
             steps {
               checkout scm
               sh 'mvn test'   
             }
         }   
     }
 }
