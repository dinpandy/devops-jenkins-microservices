//Declarative
pipeline {
	//agent {docker{ image 'maven:3.6.3'	} }
	//agent { docker{ image 'node:13.8'	} }
	agent any
	environment
	{
		mavenHome = tool 'myMaven'
		dockerHome = tool 'myDocker'
		PATH = "$mavenHome/bin:$dockerHome/bin:$PATH"
	}
	stages {
		stage('Build'){
			steps {
			echo "Build"
			sh 'mvn --version'
			sh 'docker version'
			echo "JOB NAME - $env.JOB_NAME"
			//sh 'node --version'
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