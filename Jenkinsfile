node{
   stage('MR SCM Checkout'){
	git 'https://github.com/mrizgit/my-app.git'
  }
   stage('MR Compile and Package'){
	sh 'mvn package'
}
}
