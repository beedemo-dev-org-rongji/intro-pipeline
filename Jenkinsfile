pipeline {
  agent any
  stages {
    stage('SayHello') {
      parallel {
        stage('SayHello') {
          steps {
            echo 'Hello World!'
            sh 'java -version'
          }
        }
        stage('SayHi') {
          steps {
            echo 'Hi Everyone!'
          }
        }
      }
    }
  }
}