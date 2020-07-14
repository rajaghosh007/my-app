
node {
  stage('SCM Checkout'){
  git: 'https://github.com/rajaghosh007/my-app'
}
stage('Compile-Package'){
def mvnHome = tool (name: 'MavanHome', type: 'maven') + '/bin/mvn'
sh "${mvnHome} package"
}
   
}

