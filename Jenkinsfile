pipeline {	 
	agent any	 
    	stages {     	 
    		stage("Compile") {          	 
            		steps {               	 
                		sh "mvn compile"          	 
            		}     	 
        	}     	 
            	stage ('Build') {  
                  	steps{
			    sh 'mvn clean'
			    sh 'mvn package'                   
               	 	} 
            	}
    		stage("Unit test") {          	 
        		steps {               	 
                		sh "mvn test"          	 
            		}     	 
        	}	 
    		stage("Deploy in tomcat AWS") {          	 
        		steps {            
				sh "sudo scp /home/labsuser/jenkins/workspace/BookzyProj/target/Bookzy-0.0.1-SNAPSHOT.jar ssh -i jo_key.pem ubuntu@ec2-35-168-16-196.compute-1.amazonaws.com:/opt/tomcat/webapps/Bookzy.jar"   	 
            		}     	 
        	}	 
    	}
}
