pipeline {
    agent any
    options {
    
        timeout(time: 1, unit: 'SECONDS')
    }
    stages {
   stage('Checkout') {
            steps {
             echo "Checkout stage"
            }
        }
        stage('build') {
            steps {
                 sh 'npm install' 
              sh 'npm build'
            }
        }
   stage('test') {
            steps {
                echo "Testing the application"
            }
        }
   stage('deploy') {
            steps {
                echo "Deploying the application"
            }
        }
   stage('Clean up') {
            steps {
                echo "Cleanup the application"
            }
        }
    }
}
