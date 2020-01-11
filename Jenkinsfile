pipeline{
	agent any
	stages{
		stage("Start grid"){
			steps{
				sh "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run tests"){
			steps{
				sh "docker-compose up searchmodule book-flight-module"
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'output/'
			sh "docker-compose down"
		}
	}
}