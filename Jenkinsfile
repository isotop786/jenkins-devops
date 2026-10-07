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

}