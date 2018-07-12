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
            echo "${TEST_USER_USR}"
            echo "${TEST_USER_PSW}"
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
    TEST_USER_USR = credentials('test-user')
    TEST_USER_PSW = credentials('test-password')
  }
}