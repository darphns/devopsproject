pipeline {
  agent any
  stages {
    stage('Start'){
      steps {
        echo "Pipeline Started && Login successfully "
      }
    }
    stage('Docker Build') {
      steps {
        sh 'docker build -t devopsprabin/workshop:latest .'
      }
    }
    stage('Docker Push') {
      steps {
          sh "docker login -u darphns -p 'Docker@3760'"
          sh 'docker push darphns/workshop:latest'
        }
      }
    stage('Clean docker image') {
      steps {
        sh 'docker rmi devopsprabin/workshop:latest'
      }
    }
  }
}

