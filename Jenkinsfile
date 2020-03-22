pipeline {
    agent {
        docker { image 'maven:latest' }
    }
    stages {
        stage('Test') {
            steps {
                checkout scm
                sh 'mvn package'
            }
        }
    }
}
