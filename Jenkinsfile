pipeline {
    agent any

    stages {
        stage('Compil stage') {
            steps {
                echo 'Compiling ...........'
		withMaven(maven:'Maven'){
		 sh 'mvn clean compile'}
            }
        }
        stage('Testing Stage') {
            steps {
                echo 'Testing.. This is the testing phase'
                withMaven (maven:'Maven'){
		sh 'mvn test'
		}
	    }
        }
        stage('Deploy stage') {
            steps {
                echo 'Deploying....  This is the deployment phase'
                withMaven (maven:'Maven'){
	          sh 'mvn deploy'}
	     }
        }
	
    }
}
