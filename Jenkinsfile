node{
   stage('MR SCM Checkout'){
	git 'https://github.com/mrizgit/my-app.git'
  }
   stage('MR Compile and Package'){
	   def mvnHome = tool name: 'Maven 3.4', type: 'maven'
	   sh "${mvnHome}/bin/mvn package"
   }
	stage('Slack Notification'){
	slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#pipeline', color: 'good', message: 'MR, Welcome to jenkins, Slack!', teamDomain: 'softingale', tokenCredentialId: 'sft-slack-demo'
	}
}
