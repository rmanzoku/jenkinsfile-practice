pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
	echo "Git checkout"
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
      echo 'end'
    }
  }
}
