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
