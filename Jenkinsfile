pipeline{
	agent any
	
	stages {
		stage('Compile Stage'){
			steps{
			  withMaven(maven : 'maven'){
			  	  bat 'mvn clean compile'
		      }
		    }
	   }
	   stage('Testing Stage'){
			steps{
			  withMaven(maven : 'maven'){
			  	  bat 'mvn test'
		      }
		    }
	   }
	    stage('Sonarqube Stage'){
			steps{
			  withMaven(maven : 'maven'){
			  	  bat 'mvn sonar:sonar -Dsonar.projectKey=Sample -Dsonar.host.url=http://localhost:9000 -Dsonar.login=2c436f93e92f8fe056140b1d8d7292dca8a94f0d'
		      }
		    }
	   }
	   
	   
//	   stage('Deployment Stage'){
//			steps{
//			  withMaven(maven : 'maven'){
//			  	  bat 'mvn deploy'
//	      }
//		    }
//   }
	}


}