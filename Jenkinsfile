pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building C++ Project...'
                    sh 'g++ -o PES2UG22CS327-1 main/hello.cpp'  /* Replace with your actual file */
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                    sh 'chmod +x PES2UG22CS327-1'  // Ensure execute permissions
                    sh './PES2UG22CS327-1'  // Execute compiled file
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'echo "Deployment successful!"'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Please check the logs for errors.'
        }
    }
}
