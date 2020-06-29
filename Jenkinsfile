pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent {
        docker {
          image 'gradle:6.5-jdk11'
          args '--rm -u root -v "$PWD":/home/root/project -w /home/root/project'
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