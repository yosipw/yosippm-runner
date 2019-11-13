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
				sh "docker-compose up -d db be"
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
			sh "docker-compose down"
			sh "rm -rf output/"
		}
	}
}