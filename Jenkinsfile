
node {
   // This is to demo github action	
 
   def mvn = tool (name: 'MavanHome', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    // Clone repo
	git branch: 'master', 
	credentialsId: 'github', 
	url: 'https://github.com/javahometech/myweb'
   
   }
   
}

