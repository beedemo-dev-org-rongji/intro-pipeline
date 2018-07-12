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
            echo "Hello ${params.Name}!"
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
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}