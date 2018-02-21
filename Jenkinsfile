pipeline {
    agent { docker 'php' }

    option {
      buildDiscarder(logRotator(numTokeepStr: '2', artifactsNumTokeepStr: '1'))
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
