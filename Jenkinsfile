node{
   stage('MR SCM Checkout'){
	git 'https://github.com/mrizgit/my-app.git'
  }
   stage('MR Compile and Package'){
	   def mvnHome = tool name: 'maven', type: 'maven'
	   sh "${mvnHome}/bin/mvn package"
   }
}
