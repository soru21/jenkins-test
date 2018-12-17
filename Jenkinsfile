pipeline {
  agent { 
    node {
      label 'master'
    }
  }
  stages {
    stage ('initial') {
      steps {
        echo "Hello World ${HOSTNAME}"
      }
    }
    stage ('final') {
      steps {
        echo "Bye World ${HOSTNAME}"
      }
    }
  }
}
