pipeline {
  agent any
  environment {
    MYSQL_PASSWORD = credentials('jenkins-app-mysql-password')
    MYSQL_ROOT_PASSWORD = credentials('jenkins-app-mysql_root_password')
  }
  stages {
    stage('build') {
      steps {
        sh 'docker compose build'
      }
    stage('deploy') {
      steps {
        sh 'docker compose up -d'
      }
    }
  }
}
