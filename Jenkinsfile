pipeline {
  agent any 
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-west-1',credentials:'aws-static') {

                // Upload files from working directory 'dist' in your project workspace
                s3Upload(file: 'index.html', bucket:"jenkinsbucket011", workingDir:'');
            }
      }
    }
  }
}
