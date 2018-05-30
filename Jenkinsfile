pipeline {
    agent any
	
	tools{
		maven 'maven_3_5_2'
		jdk 'java8'
	}
	
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_2') {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_2') {
                    bat 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_2') {
                    bat 'mvn deploy'
                }
            }
        }
    }
}