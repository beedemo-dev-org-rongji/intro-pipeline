pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('SayHello') {
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
         stage('Deploy') {
      input {
        message "Should we continue?"
      }
      steps {
        echo "Continuing with deployment"
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
