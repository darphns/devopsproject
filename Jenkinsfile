pipeline {
  agent any
  stages {
    stage('Start') {
      steps {
        echo "Pipeline Started && Login successfully"
      }
    }
    stage('Docker Build') {
      steps {
        script {
          sh 'docker build -t darphns/workshop:latest .'
        }
      }
    }
    stage('Clean docker image') {
      steps {
        script {
          sh 'docker rmi darphns/workshop:latest'
        }
      }
    }
  }
}

