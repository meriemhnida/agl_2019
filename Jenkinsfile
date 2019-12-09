pipeline{
agent any
	tools{
	maven 'MAVEN 3'
	jdk 'jdk1.8.0_172'
	}
	stages{
		stage('build'){
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
		stage('Test') {
            steps {
                bat 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
		stage('couverture') {
            steps {
               
                bat 'mvn cobertura:cobertura -Dcobertura.report.format=xml'
                
            }
             post {
                  always {
                        cobertura coberturaReportFile: '**/target/site/cobertura/coverage.xml'
                       
                        }
                  }
        }
	}
}
