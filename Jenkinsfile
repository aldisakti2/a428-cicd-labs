node {
    docker.image('node:16-buster-slim').inside {
	stage('Build'){
	    sh 'npm --version'
	    sh 'npm install'
	}
    
    	stage('Test'){
	    sh './jenkins/scripts/test.sh'
    	}
    }
}
