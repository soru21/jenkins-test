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
    stage ('building app.jar artifact') {
      environment {
        HELLO = 'sharma'
      }
      steps {
        echo "env.$HELLO"
      }
    }  
  }
}
