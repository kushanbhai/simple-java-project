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
         stage('Test'){
            steps{
              checkout scm
              sh 'mvn compile'
             }        
         }
      stage('Deploy'){
         steps{
            checkout scm
            sh 'mvn package'
         }
      }
   }
}
