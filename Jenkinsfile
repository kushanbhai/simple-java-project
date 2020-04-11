pipeline {
    agent any
    stages {
        stage('Example Build') {
            agent { docker { image '${myimage1}' } }
            steps {
                echo 'Hello, Maven'
                sh 'mvn --version'
            }
        }
        stage('Example Test') {
            agent { docker { image '${myimage2}' } }
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
            }
        }
    }
}
