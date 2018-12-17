pipeline {
  agent { 
    node {
      label 'master'
    }
  }
  stages {
    stage ('initial') {
      steps {
        sh '''
        #!/bin/bash
        whoami
        env
        ls -l $HOME
        '''
      }
    }
    stage ('final') {
      steps {
        echo "Bye World ${HOSTNAME}"
      }
    }
  }
}
