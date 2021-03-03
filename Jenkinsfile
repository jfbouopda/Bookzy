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
    	}
}
