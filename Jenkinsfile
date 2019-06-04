pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh './gradlew clean build'
        archiveArtifacts(artifacts: '**/build/libs/*.jar', fingerprint: true)
      }
    }
    stage('Deploy') {
      steps {
        sh 'ls build/libs/*.jar'
        echo 'Deploying...'
      }
    }
  }
}