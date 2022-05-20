pipeline {
  agent any
  stages {
    stage('build') {
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

    stage('') {
      steps {
        sh './gradlew clean build'
      }
    }

  }
}