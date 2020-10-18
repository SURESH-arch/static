pipeline {
  agent any 
  stages {
    stage(‘Build’) {
      steps {
      sh 'echo "hello world1"'
    }
    }
    stage('Upload to AWS') {
       steps {
        withAWS(region:'us-east-2',credentials:'aws-static') 
        sh 'echo "Uploading content with AWS creds"'
        s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html',bucket:'jenkinspipelineusers3')
           }
         }
       } 
     }
