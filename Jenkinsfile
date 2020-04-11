pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
        }
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
                sh 'mvn test'
            }
        }
    }
}
