pipeline {
    agent any
    stages{
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('package'){
            steps{
                sh 'mvn clean package'
            }
        }
        stage('Deploy war'){
            steps {
                echo 'deploy'
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