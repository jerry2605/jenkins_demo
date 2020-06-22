pipeline {
  agent {
    docker {
      image 'python:rc-alpine'
    }

  }
  stages {
    stage('Deploy - Staging') {
      parallel {
        stage('Deploy - Staging') {
          steps {
            echo 'staging'
            echo 'run-smoke-tests'
            sh 'python3 --version'
          }
        }

        stage('staging 2') {
          steps {
            echo 'This is staging 2'
          }
        }

      }
    }

    stage('Sanity check') {
      steps {
        input 'Does the staging environment look ok?'
      }
    }

    stage('Deploy - Production') {
      steps {
        echo 'deploy production'
        sh 'pwd'
        sh 'ls -al'
      }
    }

  }
}