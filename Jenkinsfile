pipeline {
    agent { docker 'php' }

    options {
      buildDiscarder(logRotator(numTokeepStr: '2', artifactNumTokeepStr: '1'))
    }   
    stages {
        stage('build') {
            steps {
                sh 'php --version'
              }
            }
        }

    post {
      always {
        archiveArtifacts artifacts: 'MyGod', fingerprint: true
      }

   }
}
