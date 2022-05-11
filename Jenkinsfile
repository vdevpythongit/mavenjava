pipeline {
	agent {
	  label 'maven-slave01'
	  }
		stages {
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
