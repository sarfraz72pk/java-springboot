pipeline {
    agent any 
    stages {
        stage('validate') {
            steps {
                echo 'validate'
                sh 'mvn validate'             
            }
        }
        stage('install') {
            steps {
                echo 'install'
                sh 'mvn install'             
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
                sh 'mvn test'
            }
        }
        stage('compile') {
            steps {
                echo 'compile'
            }
        }
        stage('package') {
            steps {
                echo 'package'
                sh 'mvn package'             
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