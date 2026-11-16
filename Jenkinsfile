pipeline {
    agent any
    options {
        // Changed from SECONDS to MINUTES so the build doesn't immediately abort
        timeout(time: 10, unit: 'MINUTES')
    }
    stages {
        stage('Checkout') {
            steps {
                echo "Checkout stage"
                // Note: In a real pipeline, you would use 'checkout scm' here
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
                // Added 'run' since 'build' is a custom package.json script
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
    // Moved cleanup to 'post' so it executes even if a stage fails
    post {
        always {
            echo "Cleanup the application"
            // cleanWs() // Common Jenkins step to wipe the workspace
        }
    }
}
