pipeline{
	agent any
	stages{
	   stage("Run Grid"){
		steps{
		   sh "docker-compose up -d  hub chrome firefox"
		}
}
	    stage("Run test"){
		steps{
		sh "docker-compose up search-module bookflight_module"
		}
	}


	   //stage("Bring Grid Down"){

		//steps{
			//sh "docker-compose down"
		//}

//}

	}

	post{
			always{
					archiveArtifacts artifacts: 'output/**'
					sh "docker-compose down"
			}

	}

}
