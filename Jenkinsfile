pipeline {
  agent any
  stages {
    stage('clean') {
      steps {
        bat(script: 'mvn clean', returnStatus: true)
      }
    }

    stage('compile') {
      steps {
        bat(script: 'mvn compile', returnStatus: true)
      }
    }

  }
  environment {
    mvn = 'clean'
  }
}