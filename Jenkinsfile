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
    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
