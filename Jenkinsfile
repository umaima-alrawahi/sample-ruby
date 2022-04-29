pipeline {
    agent any

    stages {
      stage('Requerment') {
            steps {
                sh 'gem install sinatra -v1.4.8'
            }
        }
        stage('Build') {
            steps {
            sh 'ruby main.rb'
            }

        }
	    
    
    }
}
