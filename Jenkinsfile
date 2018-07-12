pipeline {
  agent {
    label 'jdk8'
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