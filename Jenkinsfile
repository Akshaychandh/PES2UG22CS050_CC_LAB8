pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g+ -o PES2UG22CS050-1 PES2UG22CS050-1.cpp'
                echo 'Build Stage Successful'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES2UG22CS050-1'
                echo 'Test Stage Successful'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'echo Deploying the application'
                echo 'Deployment Successful'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
