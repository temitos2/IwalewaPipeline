pipeline {
    agent { docker 'php' }
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
