pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('SayHello') {
      parallel {
        stage('SayHello') {
          steps {
            echo 'Hello World!'
            echo "Hello ${MY_NAME}!"
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
  environment {
    MY_NAME = 'Kevin'
  }
}