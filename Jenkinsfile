
node {
  
   stage('Checkout') {
           
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rajaghosh007/my-app']]])
                sh "ls -lart ./*"
           
        }  
  
  
  
stage('Compile-Package'){
def mvnHome = tool (name: 'MavanHome', type: 'maven') + '/bin/mvn'
sh "${mvnHome} package"
}

  stage('Email Notification'){
    mail bcc: '', body: '''Hello Team ,

Jenkins build trigger
Thanks
Raja G''', cc: '', from: '', replyTo: '', subject: 'Build Triggered ', to: 'raja.ghosh123@gmail.com'
  }
   
}

