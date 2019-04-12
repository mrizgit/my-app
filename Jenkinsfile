node{
   stage('MR SCM Checkout'){
	git 'https://github.com/mrizgit/my-app.git'
  }
   stage('MR Compile and Package'){
	   def mvnHome = tool name: 'maven-3', type: 'maven'
	   sh "${mvnHome}/bin/mvn package"
   }
	stage('MR is now sending email notification') {
		mail bcc: '', body: '''Hi, Your Jenkins job have run successfully.
		Please note this is auto generated email.
		Thanks.''', cc: '', from: '', replyTo: '', subject: 'Jenkins job ran successfully', to: 'softingale@gmail.com'
	}
}
