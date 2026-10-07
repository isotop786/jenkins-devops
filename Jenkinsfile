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
	// agent { docker { image 'maven:3.6.3' } }
	// agent { docker { image 'python:3.15-rc' } }
	environment {
		dockerHome = tool 'my-docker'
		mavenHome = tool 'my-maven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage("Build"){
			steps{
					echo "Bulid"
					echo "Path: $PATH"
					echo "Build_number - $env.BUILD_NUMBER"
					echo "Build ID: $env.BUILD_ID"
					echo "Job Name: $env.JOB_NAME"
					echo "Buidl Tag - $env.BUILD_TAG"
					echo "Buidl url - $env.BUILD_URL"
					sh "mvn --version"
					sh "Docker --version"
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