pipeline {
  agent {
    docker {
      image 'adoptopenjdk/openjdk8'
    }
  }
  stages {
    stage ('build') {
      steps {
        echo 'Running build automation'
        sh 'hostname; whoami; id; java -version'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
