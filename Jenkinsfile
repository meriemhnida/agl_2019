pipeline{
agent any
	tools{
	maven 'MAVEN 3'
	jdk 'jdk1.8.0_172'
	}
	stages{
		stage('compilation'){
				steps{
				bat 'mvn compiler:compile'
				}
                        post {
                    success {
                     bat "echo 'Projet compilé avec succès'"     
                    }
                    failure {
                     bat "echo 'Erreur lors de la compilation du projet'"     
                    }
              }
		}
	}
}
