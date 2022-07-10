//Discriptive

pipeline {
	agent any
//	agent { docker { image 'maven:3.8.6'} }
	// agent { docker { image 'node:18.5'} }

	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage ('Checkout'){
			steps {
				sh "mvn --version"
				sh "docker --version"

				echo "Build"
				echo "PATH - $PATH"
				echo "Build no - $env.BUILD_NUMBER"
				echo "Build id - $env.BUILD_ID"
				echo "Build_tag - $env.BUILD_TAG"
				echo "Build_url - $env.BUILD_URL"
				echo "$env.JOB_NAME"
			}
		}
		stage ('Compile'){
			steps {
				sh "mvn clean compile"
			}
		}
		stage ('Test'){
			steps {
				sh "mvn test"
			}
		}
		stage ('Integration Test'){
			steps {
				sh "mvn failsafe:integration-test"
			}
		}
	}
	post {
		always {
			echo 'I am awesome always'
		}
		success {
			echo 'I run when you succed'
		}
		failure {
			echo 'I run when you fail'
		}
	}
}






// //Scripted
// node {
// 		echo "Build"

// 		echo "Test"

// 		echo "IntegrationTest"

// }

// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('IntegrationTest') {
// 		echo "IntegrationTest"
// 	}
// }
