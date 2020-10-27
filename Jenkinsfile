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
        bat(script: 'mvn install', returnStatus: true)
      }
    }

    stage('test') {
      steps {
        bat(script: 'mvn test', returnStatus: true)
      }
    }

  }
  environment {
    mvn = 'clean'
  }
}