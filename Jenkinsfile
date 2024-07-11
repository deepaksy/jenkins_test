pipeline {
	agent any

	stages {
	    stage('Checkout') {
	    	steps {
			git 'https://github.com/deepaksy/jenlins_test.git'
		}
	    }

	    stage('Build') {
	    	steps {
		    sh 'npm install'
		    sh 'npm run build'
		}
	    }

	    stage('Test') {
	        steps {
		    sh 'npm test'
		}
	}
}
}
