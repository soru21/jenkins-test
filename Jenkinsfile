pipeline {
  agent { 
    node {
      label 'master'
    }
  }
  environment {
    HELLO = 'anmol'
  }
  stages {
    stage ('local env') {
      environment {
        HELLO = 'sharma'
      }
      steps {
        withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', credentialsId: '2a250168-9b26-42c7-be71-c71227ceb65c']]) {
          echo "${env.AWS_ACCESS_KEY_ID}"
          echo "${env.AWS_SECRET_ACCESS_KEY}"
        }
      }
      steps {
        echo "${env.AWS_ACCESS_KEY_ID}"
        echo "${env.AWS_SECRET_ACCESS_KEY}"
        echo "${AWS_ACCESS_KEY_ID}"
        echo "${AWS_SECRET_ACCESS_KEY}"
      }
    }
    stage ('global env') {
      steps {
        echo "${env.HELLO} and ${HELLO}"
      }
    }
  }
}
