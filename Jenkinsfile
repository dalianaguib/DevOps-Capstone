pipeline {
	agent any
	stages {

		stage('Lint HTML') {
			steps {
				sh 'tidy -q -e *.html'
			}
		}
		
		stage('Build Docker Image') {
			steps {
				withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'dockerhub-cred', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD']]){
					sh '''
						 sh 'echo $PASSWORD'
  
                         echo USERNAME
 
                         echo "username is $USERNAME"
					'''
				}
			}
		}

		
		

	}
}
