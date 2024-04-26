pipeline {
  agent any
  stages {
    stage('verify version') {
      steps {
        powershell 'php --version'
      }
    }
    stage('hello') {
      steps {
        powershell 'php hello.php'
      }
    }
  }
}