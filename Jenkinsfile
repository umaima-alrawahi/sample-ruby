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
	    stage('Run production deployment') {
      when not {
        branch 'main'
      }

	     steps{
		build job: 'sample-ruby-deploy', parameters: [string(name: 'DEPLOY_TO', value: 'qa'),
							 string(name: 'upstreamJobName', value: BRANCH_NAME)]
	     }
        }
	    
	stage('Run production deployment') {
      when {
        branch 'main'
      }

      steps {
        build job: 'sample-ruby-deploy', parameters: [string(name: 'DEPLOY_TO', value: 'production'),
                                                 string(name: 'upstreamJobName', value: BRANCH_NAME)]
      }
    }
    }
}
