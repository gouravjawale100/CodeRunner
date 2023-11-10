pipeline {

agent any 

stages {

stage('execute cucumber tests'){

	steps{

		bat "docker-compose up"
	}

}

stage('Bring down compose' ){

	steps{

		bat "docker-compose down"
	}

}


}

}