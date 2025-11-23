pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Starting build process..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Executing deployment..."
            }
        }
    }

    post {
        always {
            echo 'Pipeline Completed'
        }
    }
}
