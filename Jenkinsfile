pipeline {
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Build'
                sh 'mvn package'
            }
        }
        stage('Test'){
            steps{
                echo 'Test'
                sh 'mvn test'
            }
        }
        stage('Push to artifactory'){
            steps{
                echo 'push to artifactory'
            }
        }
        stage('Deploy to QA'){
            steps{
                echo 'Deploy to QA'
            }
        }
        stage('Deploy to prod'){
            steps{
                echo 'Deploy to prod'
            }
        }
    post{
        failure{
            echo 'Build failed'
        }
        success{
            echo 'Build Success'
        }
    }
}