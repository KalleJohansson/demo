pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent {
        docker {
          image 'gradle:6.5-jdk11'
          args '--rm -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project'
        }

      }
      steps {
        withGradle() {
          sh 'gradle clean build'
        }

      }
    }

  }
}