pipeline {
	agent {docker {image maven:3.6.3'}} // This is the agent that will execute the pipeline
	stages {
		stage('Build') {
			steps {
				sh "mvn --version"
				echo "Building the app"
			}
		}	
		stage ('Test') {
			steps {
				echo "Testing the app"
			}
		}
		stage ('Integration test') {
			steps {
				echo "Integration the app"
			}
		}
	}
	post {
		always {
			echo "This will always run"
		}
		success {
			echo "This will run only if successful"
		}
		failure {
			echo "This will run only if failed"
		}
		unstable {
			echo "This will run only if the run was marked as unstable"
		}
		changed {
			echo "This will run only if the state of the Pipeline has changed"
			echo "For example, if the Pipeline was previously failing but is now successful"
		}
	}
}
