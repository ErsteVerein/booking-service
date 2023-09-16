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

    stage('Backend tests') {
      parallel {
        stage('Backend tests') {
          steps {
            sh './mvnw clean test'
          }
        }

        stage('Package') {
          steps {
            sh './mvnw clean package'
          }
        }

      }
    }

  }
}