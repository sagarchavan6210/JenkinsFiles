# JenkinsFiles
Jenkins files documents: 
https://jenkins.io/doc/book/pipeline/jenkinsfile/

Add credential into jenkins credentials and add below code into jenkinsfile.

sh```
parameters {
    credentials(name: 'CredsToUse', description: 'A user to build with', defaultValue: '', credentialType: "Username with password", required: true )
} ```

AWS configure and get creds from jenkins creds
sh```

   credentials(defaultValue: 'sagar', description: 'CloudHedge Credentials', name: 'creds-id')
   withAWS(credentials:'nameOfSystemCredentials') {
    // do something
    aws configure set aws_access_key_id ${AWS_ACCESS_KEY_ID}
    aws configure set aws_secret_access_key ${AWS_SECRET_ACCESS_KEY}
    aws configure set region ${AWS_REGION}
}
```
