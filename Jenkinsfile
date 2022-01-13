pipeline {
    // master executor should be set to 0
    agent any
	stages{
		stage('StartGrid-Docker'){
		steps{
			
			bat "docker compose up hub chrome firefox -d"
		}
		}
		stage('RunTest-Automation-Test'){
		steps{
			
			bat "docker compose up search-module book-flight"
		}
		}
		stage('StopGrid-Docker'){
		steps{
			
			bat "docker compose down"
		}
		}
    }
}