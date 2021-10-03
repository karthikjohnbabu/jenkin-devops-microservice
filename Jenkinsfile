// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 		stage('IntegrationTest') {
// 		echo "IntegrationTest"
// 	}
// }
//Declarative
pipeline{
	// agent any
	// agent { docker { image 'maven:3.6.3'}}
	agent {docker{image 'node:13.8'}}
	stages {
		
		stage('Build'){
			steps{
				sh "mvn --version"
				echo "Build"
			}
		}
stage('TEST'){
			steps{
				echo "Test"
			}
		}

		stage('IntegrationTest'){
			steps{
				echo " Integration Test"
			}
		}

	}
	post {
		always {
			echo " I am awesome, I run always"
		}
	
		success {
			echo " I run when you are successful"
	}
		failure {
			echo " I run when you fail"
	}
		changed {
			echo " I run when you fail"
	}

	}
}
