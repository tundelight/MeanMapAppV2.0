pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        sh 'echo build'
      }
    }

    stage('Backend Test') {
      parallel {
        stage('Unit Test') {
          steps {
            sh 'echo backend'
          }
        }

        stage('Performance') {
          steps {
            sh 'echo performance'
          }
        }

      }
    }

    stage('Frontend') {
      steps {
        sh 'echo frontend'
      }
    }

    stage('Static Analysis') {
      steps {
        sh 'echo stat analysis'
      }
    }

    stage('Deployment') {
      steps {
        sh 'echo deploy'
      }
    }

  }
}