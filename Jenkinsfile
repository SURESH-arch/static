pipeline {
    agent any
    stages {
        stage ('Upload to AWS') {
            steps {
                withAWS(region:'us-east-2',credentials:'awsstatic') {
                    s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html',bucket:'jenkinspipelineusers3')
                }
            }
        }
}
