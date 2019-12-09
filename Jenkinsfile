pipeline{
agent any
	tools{
	maven 'jdk1.8.0_172'
	jdk 'MAVEN 3'
	}
	stages{
		stage('build'){
				steps{
				bat 'mvn clean install'
				}
		}
	}
}