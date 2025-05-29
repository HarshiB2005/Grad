piprline {
	agent any
	
	tools {
		gradle 'Gradle'
		jdk 'JDK'
	}
	
	stages {
		stage {
			steps('Checkout') {
				git branch : 'master' , url:'https://github.com/HarshiB2005/Grad.git'
			}
		}
		
		stage {
			steps('Build') {
				sh 'gradle build'
			}
		}
		
		stage {
			steps('Test') {
				sh 'gradle test'
			}
		}
		
		stage {
			steps('Run Application') {
				sh 'gradle run'
			}
		}
	}
	
	post {
		success{
			echo 'Build and Deployment Successful'
		}
		failure{
			echo 'Build Failed'
		}
	}
}
