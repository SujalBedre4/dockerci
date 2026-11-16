pipeline {
    agent any
    options {
        timeout(time: 10, unit: 'MINUTES')
    }
    stages {
        stage('Checkout') {
            steps {
                echo "Checkout stage"
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                echo "Testing the application"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the application"
            }
        }
    }
    post {
        always {
            echo "Cleanup the application"
        }
    }
}
