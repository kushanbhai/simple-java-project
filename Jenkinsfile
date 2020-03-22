pipeline {
    agent {
        docker { image 'maven:3.6.3-jdk-11-openj9' }
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
