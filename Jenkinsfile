pipeline {
  agent any
  stages {
    stage('Build Application') { 
      steps {
        bat 'mvn clean install'
      }
    }
 	stage('Test') { 
      steps {
        echo 'Test Appplication...' 
        bat 'mvn test'
      }
    }
 	
   
	stage('Deploy Onprem') {             
      steps {
        echo 'Deploying only because of code commit...'
        echo 'Deploying to  Onprem environment....'
        bat 'mvn clean package deploy -DmuleDeploy'
      }
	  
	}
  }
}