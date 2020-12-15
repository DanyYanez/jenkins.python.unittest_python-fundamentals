// Powered by Infostretch 

timestamps {

node () {

	stage ('Python_Pipeline - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/DanyYanez/jenkins.python.unittest_python-fundamentals']]]) 
	}
	stage ('Python_Pipeline - Build') {
 			// Shell build step
sh """ 
python3 -m unittest discover -s ./src/test/ -p '*_test.py' 
 """ 
	}
}
}
