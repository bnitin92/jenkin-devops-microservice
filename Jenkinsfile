//Discriptive

pipeline {
//	agent any
	agent { docker { image 'maven:3.8.6'} }
	stages {
		stage ('Build'){
			steps {
				sh "mvn --version"
				echo "Build"
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
