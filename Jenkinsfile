pipeline {
  agent { 
    node {
      label 'docker'
    }
  }
  stages {
    stage ('clone data-platform repo') {
    }
    stage ('build App.jar') {
      environment {
        AWS_S3_BUCKET = 'st-dataplatform'
        AWS_REGION = 'us-east-1'
      }
      steps {
        withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: '4289d2bf-e8f4-446b-bd91-fde8dc19d892', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
          sh '''
          packer build build-D-P-AppDotJar.json
          '''
        }
      }
    }
  }
}
