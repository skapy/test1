pipeline {
  agent any
  stages {
    stage('Ask for parameters') {
      steps {
        echo 'Ask?'
      }
    }
    stage('Initialise pipeline tasks') {
      steps {
        echo 'create pipeline'
      }
    }
    stage('Deploying Orders') {
      parallel {
        stage('Deploying Orders Config to CI') {
          steps {
            sleep 5
          }
        }
        stage('Deploying Orders service to CI ') {
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
          steps {
            sleep 5
          }
        }
        stage('Deploying Patiens service to CI') {
          steps {
            sleep 5
            echo 'done patirents'
          }
        }
      }
    }
    stage('Clean Up & Finish') {
      steps {
        echo 'finished'
      }
    }
  }
}