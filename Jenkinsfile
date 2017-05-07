pipeline {
  agent any
  stages {
    stage('say hello') {
      steps {
        parallel(
          "say hello": {
            echo 'say hello'
            
          },
          "run script": {
            echo 'begin to run script'
            sh 'echo "run this script"'
            
          }
        )
      }
    }
  }
}