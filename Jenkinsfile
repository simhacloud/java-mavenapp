pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat(script: 'mvn clean install', returnStatus: true)
      }
    }

    stage('compile') {
      steps {
        bat(script: 'mvn install', returnStatus: true)
      }
    }

    stage('test') {
      steps {
        bat(script: 'mvn sonar:sonar', returnStatus: true)
      }
    }

  }
  environment {
    mvn = 'clean'
  }
}