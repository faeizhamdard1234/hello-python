pipeline {
	agent any 
		stages {
	   stage('Build'){
		steps {
		      echo 'Building the Python app...'
            }
        }
		stage('Test') {
            		steps {
                		sh 'pytest > result.txt'
            }
        }
		stage('Deploy') {
            steps {
                echo 'Deploying the app...'
                sh 'python3 app.py > output.txt'
                archiveArtifacts artifacts: 'output.txt', fingerprint: true
            }
        }
    }
}
