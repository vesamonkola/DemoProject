pipeline {
  agent any
  stages {
    stage('image') {
      steps {
        sh 'docker build -t demo .'
      }
    }
    stage('run docker') {
      steps {
        sh '''docker stop demo
docker rm demo
docker run --name=demo -d -t -p 3000:3000 demo'''
      }
    }
  }
}