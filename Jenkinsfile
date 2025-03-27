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
				echo "deploy is not supported yet."
			    //bat "mvn jar:jar deploy:deploy"
			}
		}
	}
}