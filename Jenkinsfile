pipeline {
  agent any

  stage {
    stage('Checkout') {
      echo "Git checkout"
    }
    stage('bundle') {
      echo "bundle install"
      echo "bundle package"
    }
    stage('asset') {
      echo "bundle exec rake assets:precompile"
    }
    stage('tar') {
      echo 'tar'
    }

  }
}
