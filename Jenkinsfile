pipeline {
	agent {  label 'linux-ec2-node' }
	stages {
		stage('---clean---'){
			tools {
				maven 'mvn-3.8.4'
			}
			steps {
				
				sh "mvn clean"
			}
		}
		stage('---test---') {
			tools {
				maven 'mvn-3.8.1'
			}
			steps {
				
				sh "mvn test"
			}
		}
		stage('---package---'){
			
			steps {
				
				sh "mvn package"
			}
		}
	}
	post {
		success {
			echo 'job was built successfully done'
		}
		failure {
			echo 'job was not build..it was failed'
		}
	}
}
