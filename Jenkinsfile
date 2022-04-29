pipeline {
    agent any
    stages {
        stage('Bulid') {
            steps {
                sh 'ruby main.rb'
            }
        }
	stage('Save artifact'){
		steps {
			archiveArtifacts artifacts: 'sample-ruby', followSymlinks: false
		}
	}
    }

}
