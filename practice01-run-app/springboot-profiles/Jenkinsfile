// Declarative syntax
pipeline {
  agent { label 'testslave' } //Configured in Jenkins > configuration > Cloud > Docker

  stages {
    stage('Build') {
      steps {
        echo 'Building app...'
        // Access env variables
        echo "Running build no. ${env.BUILD_ID} with job name: ${env.JOB_NAME} on ${env.JENKINS_URL}"
      }
    }
    stage('Test') {
      steps {
        echo 'Testing app...'
      }
    }
    stage('DockerImage') {
      steps {
        echo 'Building docker image...'
      }
    }
    stage('ImageRegistry') {
      steps {
        echo 'Pushing image to registry...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying app...'
      }
    }
  }
  // Handling events
  post {
    always {
      echo 'Executing always post action'
    }
    success {
      echo 'Executing success post action'
    }
    unstable {
      echo 'Executing unstable post action'
    }
    failure {
      echo 'Executing failure post action'
    }
    changed {
      echo 'Executing changed post action'
    }
  }
}
