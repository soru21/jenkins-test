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
        while $(dpkg -l zip 1>/dev/null 2>&1)
        do
          apt-get update
          apt-get install zip -y -qq
        done
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
