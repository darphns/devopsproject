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
          sh "docker login -u devopsprabin -p '%41ry&i*bs#5P7NU12'"
          sh 'docker push devopsprabin/workshop:latest'
        }
      }
    stage('Clean docker image') {
      steps {
        sh 'docker rmi devopsprabin/workshop:latest'
      }
    }
  }
}

