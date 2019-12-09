pipeline{
agent any
	tools{
	maven 'MAVEN 3'
	jdk 'jdk1.8.0_172'
	}
	stages{
		stage('build'){
				steps{
				bat 'mvn clean install'
				}
		}
	}
}
