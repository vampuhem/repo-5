pipeline {
	agent  any
	tools {
		gradle 'Gradle-6.2'
	}
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
			withGradle(){
			sh './gradelw -v'
			}
                }
        }
	}
}
