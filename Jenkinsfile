pipeline{
  agent any
  stages{
    stage ('Clone repo') {
    steps{
      withEnv(['PATH+EXTRA=/usr/sbin:/usr/bin:/sbin:/bin']) {  
       sh "export AWS_DEFAULT_REGION=us-east-1"
      sh "aws cloudformation --create-stack --stack-name myteststack --template-body file://s3bucket.json --region 'us-east-1'"
      }
      }
    }
  }
}
