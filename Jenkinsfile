pipeline {

agent any 

stages {

	stage('pull the image'){

	steps{

		bat "docker pull atttest/entireconfigurationinyamlimage"
	}

}

stage('Starting the grid'){

	steps{

		bat "docker-compose up -d hub chrome firefox"
	}

}

stage('Executing cucumber testcases'){

	steps{

		bat "docker-compose up cucumbertestcases"
	}

}

}

post{

always{
	bat "docker-compose down"
}


}

}