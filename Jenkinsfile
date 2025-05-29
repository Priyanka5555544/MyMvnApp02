pipeline{
    agent any
	
    tools{
        maven 'Maven'
	}
    stages{
	stage('checkout'){
	    steps{
	    	git branch:'master',url:'https://github.com/Priyanka5555544/MyMvnApp02.git'
	    	}
	    }
	stage('Build'){
	    steps{
	    	sh 'mvn clean package'
	    	}
	 }
	stage('Test'){
	    steps{
	       sh 'mvn test'
	       }
	 }
	 stage('Aplication run'){
	     steps{
	         sh 'java -jar target/MyMvnApp02-1.0-SNAPSHOT.jar'
	         }
	 }
}
post{
	sucess{
		echo 'build and deploy sucess'
		}
	fail{
	echo 'build fail'
	}
	}
	}
				
		
