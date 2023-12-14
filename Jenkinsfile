node {
    checkout scm
    stage('Build'){
	docker.image('node:16-buster-slim').withRun('-p 3000:3000').inside {
	    sh 'npm --version'
	    sh 'npm install'
	}
    }
    stage('Test'){
	sh './jenkins/scripts/test.sh'
    }
}
