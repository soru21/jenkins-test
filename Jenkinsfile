pipeline {
  agent { 
    node {
      label 'master'
    }
  }
  stages {
    stage ('building app.jar artifact') {
      steps {
        sh '''
        if [ -f /bin/packer ]; then
          wget http://example.com/packer.zip
          unzip packer.zip
          mv packer /bin
        fi
        packer build build-D-P-AppDotJar.json
        '''
      }
    }
    stage ('push app.jar to s3 bucket') {
      steps {
        sh '''
        aws s3 cp /tmp/app.jar s3://example-dp/jar/
        aws s3 cp /tmp/app.jar s3://example-dp/latest-env.jar
        '''
      }
    }
  }
}
