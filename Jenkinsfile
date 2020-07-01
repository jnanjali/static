pipeline {
  agent any 
  stages {
    stage('Upload to AWS') {
      steps {
        files = findFiles(glob: '*.html')

      files.each { 
      println "RPM:  ${it}"
      withAWS(region:'us-west-1',credentials:'aws-static'){
       s3Upload(file:"${it}", bucket:'jenkinsbucket011', path:"${bucket_path}")
        }
    }
       
      }
    }
  }
}
