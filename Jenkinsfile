pipeline{
	agent any
	stages{
	   stage("Run test"){
		steps{
		   sh "docker-compose up -d --no-color hub chrome firefox"
		   sh "docker-compose search-module bookflight-module"		
		}
	}
	   stage("Bring Grid Down"){

		steps{
			sh "docker-compose down"
		}
} 			

	}

}
