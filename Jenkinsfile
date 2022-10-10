pipeline {
    // where or who 1
    agent any
    
    // collection of stages
    stages{
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn clean package -Dmaven.test.skip=true'
            }
        }
        stage('Deploy war'){
            steps{
                echo 'Deploy'
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