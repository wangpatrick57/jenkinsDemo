pipeline {
    agent any

    stages {
	stage('Test') {
	    steps {
		sh '''
		pwd
		ls
		make
		./output
		'''
	    }
	}
    }

    post {
	always {
	    junit 'build/reports/**/*.xml'
	}
    }
}
