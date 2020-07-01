pipeline {
  agent any 
  stages {
    stage('Upload to AWS') {
        withAWS(region:'us-west-1',credentials:'aws-static') {

                 def identity=awsIdentity();//Log AWS credentials

                // Upload files from working directory 'dist' in your project workspace
                s3Upload(bucket:"jenkinsbucket011", workingDir:'', includePathPattern:'**/*');
            }
    }
  }
}
