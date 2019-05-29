pipeline {
    agent { dockerfile true }
    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                def scannerHome = tool 'SonarQube Scanner 2.8';
                withSonarQubeEnv('My SonarQube Server') {
                  sh "${scannerHome}/bin/sonar-scanner"
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
}
