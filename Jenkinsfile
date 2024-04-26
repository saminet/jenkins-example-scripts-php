pipeline {
  agent any
  stages {
    stage('verify version') {
      steps {
        php --version
      }
    }
    stage('hello') {
      steps {
        php hello.php
      }
    }
  }
}