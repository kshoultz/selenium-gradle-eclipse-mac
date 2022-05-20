pipeline {
  agent any
  stages {
    stage('Information Step') {
      parallel {
        stage('build') {
          steps {
            echo 'Initial pipeline commit.'
          }
        }

        stage('Log Tools') {
          steps {
            sh '''java --version
./gradlew -v
'''
          }
        }

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