
node {
  
   stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rajaghosh007/my-app']]])
                sh "ls -lart ./*"
            }
        }  
  
  
  
stage('Compile-Package'){
def mvnHome = tool (name: 'MavanHome', type: 'maven') + '/bin/mvn'
sh "${mvnHome} package"
}
   
}

