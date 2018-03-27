pipeline {
  agent any
  stages {
    stage('checkout') {
      parallel {
        stage('checkout') {
          steps {
            sh 'whoami'
          }
        }
        stage('') {
          steps {
            sh 'ls -lh'
          }
        }
      }
    }
    stage('check-python') {
      parallel {
        stage('check-python') {
          steps {
            sh 'which python'
          }
        }
        stage('') {
          steps {
            sh 'pwd'
          }
        }
      }
    }
    stage('build') {
      steps {
        echo 'Building ...'
      }
    }
    stage('Notify') {
      steps {
        mail(subject: 'New Jenkins build', body: 'Hi there is a new Jenkins build here!', from: 'saad.zaher@hpe.com', replyTo: 'saad.zaher@hpe.com', to: 'pegasus@lists.osp.hpe.com ')
      }
    }
  }
}
