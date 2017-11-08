pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh './gradlew compileJava'
            }
        }

        stage('Test') {
            steps {
                sh './gradlew test || true'
                junit 'build/test-results/test/*.xml'
            }
        }
    }
}