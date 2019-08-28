pipeline {
  agent any
  stages {
    stage('Ask for parameters') {
      agent any
      steps {
        echo 'Ask?'
      }
    }
    stage('Initialise pipeline tasks') {
      agent any
      steps {
        echo 'create pipeline'
      }
    }
    stage('Deploying Orders') {
      parallel {
        stage('Deploying Orders Config to CI') {
          agent any
          steps {
            sleep 5
          }
        }
        stage('Deploying Orders service to CI ') {
          agent any
          steps {
            sleep 5
            echo 'done orders'
          }
        }
      }
    }
    stage('Deploying patiens service to CI') {
      parallel {
        stage('Deploying Patiens Config to CI') {
          agent any
          steps {
            sleep 5
          }
        }
        stage('Deploying Patiens service to CI') {
          agent any
          steps {
            sleep 5
            echo 'done patirents'
          }
        }
      }
    }
    stage('Clean Up & Finish') {
      agent any
      steps {
        echo 'finished'
      }
    }
  }
}