
node ('mulesoft') {
  stage ('prebuild') {
    git credentialsId: 'c8d0bb4e-36db-4983-a29f-35e9f7878869', url: 'https://github.com/devopsstk/sabreHelloWorld.git'
  }
  stage ('build') {
  	sh 'mvn clean install'
  }
  stage ('deploy') {
  	sh """
  	
  	anypoint-cli --username=msardinas --password=Sardinas1
  	
  	runtime-mgr cloudhub-application modify hwt ${WORKSPACE}/target/hello-world_1.4.0-1-1.0.0-SNAPSHOT.zip
	  	
"""

  }
}
