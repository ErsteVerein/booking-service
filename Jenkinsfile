pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/ErsteVerein/booking-service', branch: 'main', changelog: true)
      }
    }

    stage('list files') {
      steps {
        sh 'ls -lah'
      }
    }

  }
}