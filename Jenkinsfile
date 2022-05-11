pipeline {
	agent {
	  label 'maven-slave01'
	  }
		stages {
		stage('checkoutSCM'){
			steps{
			git branch: 'main', credentialsId: 'git-password', url: 'https://github.com/vdevpythongit/mavenjava.git'
			}
		}
		 stage('Build') {
		   steps {
             sh '''
			   mvn clean install
			 '''
			}
		}
		 stage("test"){
		   steps {
		     echo "this is test"
			}
			}
		stage('Production'){
		steps {
      echo "Deploying in Prod"
		}
 }
 }
}
