pipeline {
	agent  any
	stages {
	stage('run frontend') {
		steps {
			echo "Building frontend"
			Nodejs('Node-10.17'){
			sh 'yarn install'
			}
		}
	}
	stage('run backendend') {
                steps {
                        echo "Building backend"
			withgradle(){
			sh './gradelw -v'
			}
                }
        }
	}
}
