# JenkinsFiles
Jenkins files documents: 
https://jenkins.io/doc/book/pipeline/jenkinsfile/

Add credential into jenkins credentials and add below code into jenkinsfile.
parameters {
    credentials(name: 'CredsToUse', description: 'A user to build with', defaultValue: '', credentialType: "Username with password", required: true )
} 
