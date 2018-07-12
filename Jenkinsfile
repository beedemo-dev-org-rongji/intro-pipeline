pipeline {
  agent {
    label 'jdk9'
  }
  stages {
    stage('SayHello') {
      steps {
        echo 'Hello World!'
        sh 'java -version'
      }
    }
  }
}