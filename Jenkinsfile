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
            
          },
          "echo time1": {
            timestamps() {
              sh 'date'
              sleep 1
              sh 'date'
            }
            
            
          },
          "echo time2": {
            sh 'date'
            timestamps() {
              sleep 5
              sh 'date'
              timestamps() {
                sh 'echo "hello world"'
              }
              
            }
            
            
          }
        )
      }
    }
  }
}