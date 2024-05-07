pipeline {
  agent any
  stages {
    stage('verify version') {
      steps {
        powershell 'php --version'
      }
    }
    stage('Software versions') {
        steps {
            script {
                def response = input message: 'Should we print the software version',
                parameters: [
                    choice(choices: 'Yes\nNo',
                    description: 'Processd or Abort ?',
                    name: 'What to do ???'
                )]
                if(response=='Yes'){
                    bat 'git --version'
                    bat 'cd C:/maven-3.9.6/bin && mvn --version'
                    bat 'cd C:/Gradle/gradle-8.7/bin && gradle -version'
                }
            }

        }
    }
    stage('hello') {
      steps {
        powershell 'php hello.php'
      }
    }
  }
}
