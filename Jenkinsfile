pipeline {
  agent {master}
  stages {
    stage ('initial') {
      steps {
        echo "Hello World ${HOSTNAME}"
      }
      steps {
        echo "Intermediate World ${HOSTNAME}"
      }
    }
    stage ('final') {
      steps {
        echo "Bye World ${HOSTNAME}"
      }
    }
  }
}
