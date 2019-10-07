pipeline {
  agent any
  stages {
    stage('Ask for parameters') {
      agent {
        node {
          label 'linux'
        }

      }
      environment {
        test1 = '2'
        test2 = 'Darek'
        test3 = '5'
      }
      steps {
        echo 'Ask?'
        withAnt(installation: '1.9.9', jdk: '1.8') {
          withAnt()
        }

      }
    }
  }
}