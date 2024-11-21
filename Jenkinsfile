pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        script {
          sh 'dotnet build YourApiProjectName.sln'
        }
      }
    }
    stage('Docker Build') {
      steps {
        script {
          sh 'docker build -t your-api-image-name .'
        }
      }
    }
    stage('Deploy to Staging') {
      steps {
        script {
          sh 'docker-compose up --build -d'
        }
      }
    }
  }
}
