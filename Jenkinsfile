pipeline {
    agent {
        docker {
            image 'openjdk:8u171-jdk-alpine'
        }
    }
  stages {
    stage ('build') {
      steps {
        echo 'Running build automation'
        sh 'hostname; whoami; id'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
