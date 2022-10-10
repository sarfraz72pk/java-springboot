pipeline {
    agent any
    stages{
        stage('build'){
            steps{
                echo 'build'
                sh 'mvn clean package'
            }
        }
        stage('Test'){
            steps{
                echo 'test'
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