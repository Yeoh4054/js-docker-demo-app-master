pipeline {
  agent any

  tools {
    gradle 'Gradle-8.14.3'
  }
  
  stages {
    stage("run frontend") {
      steps {
        echo 'executing yarn...'
        nodejs('Node-24.3') {
          sh 'yarn install'
        }
      }
    }
    stage("run backend") {
      steps {
        echo 'executing gradle...'
        sh './gradlew -v'
      }
    }
  }
}
