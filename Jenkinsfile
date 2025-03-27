pipeline {
	agent any

	environment {
        NAME = 'John'
        LASTNAME = 'Doe'
        mavenHome = tool 'jenkins-maven'
    }

	tools {
		jdk 'jenkins-jdk'
	}
    

	stages {

		stage('Build'){
			steps {
				bat "mvn clean install -DskipTests"
			}
		}

		stage('Test'){
			steps{
				bat "mvn test"
			}
		}

		stage('Deploy') {
			steps {
			    bat "mvn jar:jar deploy:deploy"
			}
		}
	}
}