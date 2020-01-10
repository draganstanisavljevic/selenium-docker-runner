pipeline{
	agent any
	stages{
		stage("Run tests"){
			steps{
				sh "docker-compose up"
			}
		}
		stage("Bring grid down"){
						steps{
				sh "docker-compose down"
			}
		}
	}
}