pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/idevcs/Bookstore.git', branch: 'main')
      }
    }

    stage('Shell') {
      steps {
        sh 'ls -la'
      }
    }

  }
}