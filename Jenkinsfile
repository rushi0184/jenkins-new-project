pipeline {
  agent any
  stages {
    stage('Package index.html') {
      steps {
        sh 'zip -r index.zip rushi/index.html'
      }
    }
    stage('Upload to S3') {
      steps {
        sh 'aws s3 cp index.zip s3://rushi-proj/'
      }
    }
  }
}
