pipeline {
    agent any 
    stages {
        stage('package') {
            steps {
                echo 'package'
                sh 'mvn package'             
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
                sh 'mvn test'
            }
        }
        stage('install') {
            steps {
                echo 'install'
                sh 'mvn install'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
                sh 'mvn deploy'             
            }
        }
        stage('Deploy to QA') {
            steps {
                echo 'Deploy to QA'
            }
        }
        stage('Deploy to Prod') {
            steps {
                echo 'Deploy to Prod'
            }
        }
    }
    post {
      failure {
        echo 'Failed'
      }
      success {
        echo 'Success'
      }
      aborted {
        echo 'aborted'
      }
    }
}