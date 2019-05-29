pipeline {
    agent { dockerfile true }
    stages {
        stage('SonarQube analysis') {
          environment {
          scannerHome = tool 'SonarQube Scanner 7.7';
            steps {
              withSonarQubeEnv('SonarQube') {
                sh "${scannerHome}/bin/sonar-scanner"
              }
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
