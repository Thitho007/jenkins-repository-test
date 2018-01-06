pipeline {
  agent any
  stages {
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'stage is TEST'
            sh 'echo toto'
          }
        }
        stage('test parallel1') {
          steps {
            echo 'parallel1'
            sh 'echo parallel1'
          }
        }
      }
    }
    stage('Deployment') {
      steps {
        sh 'echo Deployment'
        echo 'Deployment'
      }
    }
  }
  environment {
    STATUS = 'OK'
    TEST = 'true'
  }
}
