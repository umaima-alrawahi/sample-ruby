pipeline {
    agent any
    stages {
        stage('Bulid') {
            steps {
                sh 'go build -o sample-ruby main.rb'
            }
        }
	stage('Save artifact'){
		steps {
			archiveArtifacts artifacts: 'sample-ruby', followSymlinks: false
		}
	}
    }

}
