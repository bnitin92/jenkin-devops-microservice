//Discriptive

pipeline {
	agent any
//	agent { docker { image 'maven:3.8.6'} }
	// agent { docker { image 'node:18.5'} }
	stages {
		stage ('Build'){
			steps {
//				sh "mvn --version"
				// sh "node --version"

				echo "Build"
				echo "PATH - $PATH"
				echo "Build no - $env.BUILD_NUMBER"
				echo "Build id - $env.BUILD_ID"
				echo "Build_tag - $env.BUILD_TAG"
				echo "$env.JOB_NAME"
			}
		}
		stage ('Test'){
			steps {
				echo "Test"
			}
		}
		stage ('ITest'){
			steps {
				echo "ITest"
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
