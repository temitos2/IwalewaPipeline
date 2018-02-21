pipeline {
    stages {
      stage('Say Hello') {
        agent any

        steps {
          sayHello 'Awesome God' 
        }

    agent { docker 'php' }

    options {
      buildDiscarder(logRotator(numToKeepStr: '2', artifactNumToKeepStr: '1'))
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
