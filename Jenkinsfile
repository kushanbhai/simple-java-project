pipeline {
     agent { docker 'maven:3-alpine' }
     stages {
          stage('Build') {
             steps {
                try{ 
                 checkout scm
                 sh 'mvn test'
             }
                 catch(caughtError) { 
                   deleteDir();
                   sh 'mvn test'
                   checkout scm
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
