pipeline{
	agent any
	stages{
		stage("Pull Latest Image"){
			steps{
				sh "docker pull yosua161/ppm-be"
			}
		}
		stage("Start App"){
			steps{
				sh "docker-compose up"
			}
		}
	}
}