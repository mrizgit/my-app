node{
   stage('MR SCM Checkout'){
	git 'https://github.com/mrizgit/my-app.git'
  }
   stage('MR Compile and Package'){
	   def mvnHome = tool name: 'Maven 3.4', type: 'maven'
	   sh "${mvnHome}/bin/mvn package"
   }
}
