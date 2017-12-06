pipeline {
	agent any
	
	stages {
	
		stage('Git') {
			steps {
				bat 'git fetch'
			}
		}
		stage('Build') {
			steps {
				bat 'mvn -B -DskipTests clean package'
			}
		}
		stage('Test') {
			steps {
				bat 'mvn test'
			}
		}
		stage('Target') {
			steps {
				bat 'dir /S target'
			}
		}
		
		stage('Tomcat') {
			steps {
				bat 'mvn tomcat:deploy'
			}
		}
	}
}