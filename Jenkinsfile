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
    stage('Docker Push') {
      steps {
            sh "docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD"
            sh 'docker push darphns/workshop:latest'
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

