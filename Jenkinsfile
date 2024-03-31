pipeline {
  agent any
  stages {
    stage('Clone Repository') {
      steps {
        git 'https://github.com/vipin2411/simple-node-app.git'
      }
    }
    stage('Build Image') {
      steps {
        sh 'docker build -t simple-node-app .'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker run -d -p 3000:3000 --name simple-node-app-container simple-node-app'
        echo 'Application is running at http://localhost:3000'
      }
    }
  }
}
