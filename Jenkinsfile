pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'mvn 3.5.4'){
                        sh "mvn clean compile"
			input('Do you want to Proceed')
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'mvn 3.5.4'){
                        sh "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'mvn 3.5.4'){
                        sh "mvn deploy"
                }

            }
        }
    }
}
