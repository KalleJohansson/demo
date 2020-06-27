pipeline {
  agent any
  stages {
    stage('error') {
      agent {
        docker {
          image 'gradle:6.5-jdk11'
          args '--rm -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project'
        }

      }
      steps {
        sh 'gradle clean build'
      }
    }

  }
}