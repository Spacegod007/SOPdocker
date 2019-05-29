pipeline {
    agent { dockerfile true }
    stages {
        stage('SonarQube analysis') {
          environment {
            scannerHome = tool 'SonarQube Scanner 3.3.0.1492';
          }
          steps {
            withSonarQubeEnv('SonarQube Scanner 3.3.0.1492') {
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
