//Declarative
pipeline {
	agent any
	stages {
		stage('Build'){
			steps {
			echo "Build"
		}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
			
		}
		stage("Integration Test"){
			steps {
				echo "Integration Test"
			}
			
		}
	}
	post{
		always{
			echo "I execute always"
		}
		success{
			echo "I execute during successful build"
		}
		failure{
			echo "I execute during failed build"
		}
		changed{
			echo "I execute during changed build"
		}
	}
}