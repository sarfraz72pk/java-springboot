pipeline {
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Build'
                sh 'mvn clean package'
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