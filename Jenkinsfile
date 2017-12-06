pipeline {
	agent any
	
	stages {
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
	}
}