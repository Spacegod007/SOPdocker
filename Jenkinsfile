pipeline {
    agent { dockerfile true }
    stages {
        stage('SonarQube analysis') {
          steps {
              def scannerHome = tool 'SonarQube Scanner 7.7';
              withSonarQubeEnv('SonarQube') {
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
