pipeline {
  agent { 
    node {
      label 'master'
    }
  }
  withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', credentialsId: '2a250168-9b26-42c7-be71-c71227ceb65c']]) {
    echo "${env.AWS_ACCESS_KEY_ID}"
    echo "${env.AWS_SECRET_ACCESS_KEY}"
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
        echo "${env.HELLO} and ${HELLO}"
      }
    }
    stage ('global env') {
      steps {
        echo "${env.HELLO} and ${HELLO}"
      }
    }
  }
}
