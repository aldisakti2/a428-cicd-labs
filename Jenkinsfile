node {
    docker.image('node:16-buster-slim').withRun('-p 3000:3000').inside {
	checkout scm
	stage('Build') {
	    dir('/home/dicoding/ci-cd/a428-cicd-labs'){
	    	sh 'npm --version'
            	sh 'npm install'
	    }
        }
        stage('Test') {
	    dir('/home/dicoding/ci-cd/a428-cicd-labs'){
            	sh './jenkins/scripts/test.sh'
	    }
        }
    }
}
