pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/idevcs/Bookstore.git', branch: 'main')
      }
    }

    stage('Shell') {
      parallel {
        stage('Shell') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Test') {
          steps {
            sh 'docker-compose up -d --build && docker-compose exec web python manage.py test'
          }
        }

      }
    }

  }
}