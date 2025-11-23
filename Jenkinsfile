pipeline {
    agent any

    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run Tests Stage?')
    }

    stages {
        stage('Build') {
            steps {
                echo "Starting build process..."
            }
        }

        stage('Test') {
            when {
                expression { params.executeTests == true }
            }
            steps {
                echo 'Testing with conditions...'
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
