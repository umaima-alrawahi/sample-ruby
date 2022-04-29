pipeline {
    agent any
    stages {
        stage('Bulid') {
            steps {
                sh 'go build -o sample main.rb'
            }
        }
	stage('Save artifact'){
		steps {
			archiveArtifacts artifacts: 'sample', followSymlinks: false
		}
	}
    }

}
