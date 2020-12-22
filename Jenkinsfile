pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'git clone https://github.com/shreyajarsania/jenkins.git'
            }   sh 'echo "cloned"'

	    }
	stage('next'){
	steps{
		sh 'cd jenkins'
	    }	sh 'echo "entered"'
	}
	stage('deploy'){
	steps{
	   	sh 'python3 Python.py'
		sh 'echo "done"'
	   }
	}
    }
}
