pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'git clone https://github.com/shreyajarsania/jenkins.git'
                sh 'echo "cloned"'
            }
        }
        stage('Test') { 
            steps {
                sh 'cd jenkins'
                sh 'echo "entered"'

            }
        }
        stage('Deploy') { 
            steps {
                sh 'python3 Python.py'
                sh 'echo "done"'
            }
        }
    }
}
