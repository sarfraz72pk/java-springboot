pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing code'
            }
        }
        stage('Sonarqube') {
            steps {
                echo 'sonarqube'
            }
        }
        stage('Push to artifactory') {
            steps {
                echo 'Push to artifactory'
            }
        }
        stage('Deploy to QA') {
            steps {
                echo 'Deploy to QA'
            }
        }
        stage('Deploy to prod') {
            steps {
                echo 'Deploy to Prod'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        aborted { 
            echo 'Aborted'
        }
        failure { 
            echo 'Failed!'
        }
        success { 
            echo 'Succesed'
        }
    }
}