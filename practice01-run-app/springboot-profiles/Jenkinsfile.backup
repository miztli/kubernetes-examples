pipeline {
  agent none
  stages {
    stage('Test Stage') {
      agent {
        docker { image 'gradle:4.8.1-jdk8-alpine' }
      }
      steps {
        echo 'Testing stage'
      }
    }
  }
}
