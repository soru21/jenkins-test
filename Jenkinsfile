pipeline {
  agent { 
    node {
      label 'master'
    }
  }
  stages {
    stage ('branch name') {
      steps {
        echo "multibranch branch name : ${BRANCH_NAME}"
      } 
    }
  }
}
