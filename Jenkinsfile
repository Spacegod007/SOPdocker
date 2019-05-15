pipeline {
    agent { docker { image 'python:2.7-slim' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}
