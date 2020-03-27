pipeline {
    
    agent any
    
    environment {
        gitURL = 'https://github.com/heythatisz00/development.git'
        branch = 'master'
    }
    
    
    stages {
        stage('GitHub Code Checkout') {
            steps {
				echo "*****Checkout code*****"	
				//Delete everything in workspace to start fresh
				deleteDir()
				//Checkout the code
				git branch: "${branch}", url: "${gitURL}"
			}
        }
		stage('Printing Workspace') {
		    steps {
		         echo "${WORKSPACE}"
		         sh "ls"
		    }
		}
    }
}
