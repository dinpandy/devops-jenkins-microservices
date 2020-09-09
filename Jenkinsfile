//Declarative
pipeline {
	agent {
		//docker{ image 'maven:3.6.3'	} }
		docker{ image 'node:13.8'	} }
	stages {
		stage('Build'){
			steps {
			echo "Build"
			//sh 'mvn --version'
			sh 'node --version'
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