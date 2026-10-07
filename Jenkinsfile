// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Production') {
// 		echo "It running the production"
// 	}
// }


// DECLARATIVE
pipeline {
	agent any
	stages {
		stage("Build"){
			steps{
					echo "Bulid"
			}
		}
		stage("Test"){
			steps{
					
					echo "Test"
					
			}
		}
		stage("Integration Test"){
			steps{
					echo "Integration Test"
			}
		}
	} 
	
	post {
		always {
			echo "The is the post running all the time"
		}
		success {
			echo "The is the success running when there's a success"
		}
		failure {
			echo "The is the failure running when there's a failure"
		}

	}

}