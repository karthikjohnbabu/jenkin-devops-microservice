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

}
