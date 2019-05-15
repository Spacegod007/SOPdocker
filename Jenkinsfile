Jenkinsfile (Declarative Pipeline)
pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('build') {
            steps {
                bat 'docker run -p 4000:80 friendlyhello'
            }
        }
    }
}
