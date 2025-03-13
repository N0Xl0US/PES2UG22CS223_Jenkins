pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o PES2UG22CS223' 
            }
        }
        stage('Test') {
            steps {
                sh './PES2UG22CS223'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying application..."'
            }
        }
        // Added a cleanup stage
        stage('Cleanup') {
            steps {
                sh 'rm -f PES2UG22CS223' 
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
        success {
            echo 'Pipeline Succeeded' 
        }
    }
}
