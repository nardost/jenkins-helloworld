pipeline {
	agent any
	
	stages {
		stage('Build') {
			steps {
				sh 'mvn build'
			}
		}
		stage('Test') {
			steps {
				sh 'ls -lah'
				junit 'reports/**/*.xml'
			}
		}
		stage('Deploy') {
			steps {
				sh '''
					echo "Multiline shell steps."
					netstat -nl46
				'''
			}
		}
	}
 }