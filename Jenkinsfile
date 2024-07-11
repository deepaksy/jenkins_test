pipeline {
	agent {
		docker {
			image 'node:14'
			label 'my-docker-nodejs'
			args '-u root'
    }
  }

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

        post {
	    success {
	    	echo 'Pipeline succeeded!'
	    }
	    faliure {
	        echo 'Pipeline failed :('
	    }

	}
}
}
