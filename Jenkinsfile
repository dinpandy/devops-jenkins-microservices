//Declarative
pipeline {
	agent any
	stages {
		stage('Build'){
			echo "Build"
		}
		stage('Test'){
			echo "Test"
		}
		stage("Integration Test"){
			echo "Integration Test"
		}
	}
	post{
		always{
			echo "I execute always"
		}
		success{
			echo "I execute during successful build"
		}
		fail{
			echo "I execute during failed build"
		}
		changed{
			echo "I execute during changed build"
		}
	}
}