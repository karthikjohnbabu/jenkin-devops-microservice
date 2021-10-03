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
	agent any
	// agent { docker { image 'maven:3.6.3'}}
	// agent {docker{image 'node:13.8'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		
		stage('Checkout'){
			steps{
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo "BUILD_PATH- $PATH"
				echo "BUILD_NUMBER- $env.BUILD_NUMBER"
				echo "BUILD_ID- $env.BUILD_ID"
				echo "JOB_NAME- $env.JOB_NAME"
				echo "BUILD_TAG- $env.BUILD_TAG"
				echo "BUILD_URL- $env.BUILD_URL"
			}
		}
		stage('compile'){
			steps{
				sh "mvn clean compile"
			}
		}
		stage('TEST'){
			steps{
				sh "mvn test"
			}
		}

		stage('IntegrationTest'){
			steps{
				echo "mvn failsafe:integration-test failsafe:verify"
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
