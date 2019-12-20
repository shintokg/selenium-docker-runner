pipeline{
	agent any
	stages{
	   stage("Run Grid"){
		steps{
		   sh "docker-compose up -d  hub chrome firefox"
		}
	    stage("Run test"){
		step{		   
		sh "docker-compose search-module bookflight-module"		
		}
	}
		}
	}
	   stage("Bring Grid Down"){

		steps{
			sh "docker-compose down"
		}
} 			

	}

}
