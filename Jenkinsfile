pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Removed the semicolon and added better spacing
                git branch: 'main', url: 'https://github.com/gc2701p-web/claculator-.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'javac Calculator.java'
            }
        }

        stage('Build/Run') {
            steps {
                echo "Running Calculator with initial parameters..."
                sh 'java Calculator 25 5'
            }
        }

        stage('Test') {
            steps {
                echo "Testing Calculator with secondary parameters..."
                sh 'java Calculator 30 5'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline execution finished.'
        }
        failure {
            echo 'Something went wrong! Check the console output.'
        }
    }
}
