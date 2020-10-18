pipeline {
  agent any 
  stages {
    stage(‘Build’) {
      steps {
      sh 'echo "hello world"'
    }
    }
    stage('Upload to AWS') {
       steps {
        withAWS(region:'us-east-2',credentials:'awsstatic') 
        sh 'echo "Uploading content with AWS creds"'
        s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html',bucket:'jenkinspipelineusers3')
           }
         }
       } 
     }
