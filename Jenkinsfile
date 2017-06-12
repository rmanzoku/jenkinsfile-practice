pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
	echo "Git checkout"
	sh 'env'
      }
    }
    stage('bundle') {
      steps {
	echo "bundle install"
	echo "bundle package"
      }
    }
    stage('asset') {
      steps {
	echo "bundle exec rake assets:precompile"
      }
    }
    stage('tar') {
      steps {
	echo 'tar'
      }
    }

  }
  post {
    always {
      slackSend "started ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)"
    }
  }
}
