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
pipeline {
	agent any
	stages {
		stage('Build'){
			steps{
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

	}
}
