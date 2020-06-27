pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent any
      steps {
        withGradle() {
          sh 'gradle clean build'
        }

      }
    }

  }
}