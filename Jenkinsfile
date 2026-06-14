pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
		}
	stages{
		stage('checkout'){
			steps{
				git branch:'master', url:'https://github.com/shreya20m/ga.git'
			}
			}
		stage('build'){
			steps{
				sh'gradle build'
			}
		}
		stage('test'){
			steps{
				sh'gradle test'
			}
		}
		stage('run application'){
			steps{
				sh'gradle run'
			}
		}
	}
	post{
		success{
			echo 'success'
		}
		failure{
			echo 'failure'
		}
}
}
