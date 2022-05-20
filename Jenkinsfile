pipeline {
  agent any
  stages {
    stage('Log Tools') {
      steps {
        sh '''java --version
./gradlew -v
'''
      }
    }

    stage('Build Step') {
      steps {
        sh './gradlew clean build'
      }
    }

    stage('Test Step') {
      steps {
        sh './gradlew clean test'
      }
    }

  }
}