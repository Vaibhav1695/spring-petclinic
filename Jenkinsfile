
pipeline{
  	agent { label 'JDK17' }
	stages{
		stage('pull git code'){
    		     steps{ 
			 	 git branch: 'test1', url: 'https://github.com/Vaibhav1695/spring-petclinic.git'
                            }
		}
     		stage('build the code maven ' ){
		     steps{
		         	sh '''mvn clean package'''                   

			}	
 		}

		stage('artifacts and archvie'){
		    steps{
                                junit stdioRetention: '', testResults: '**/surefire-reports/*.xml'

			}
		}
	}

}






