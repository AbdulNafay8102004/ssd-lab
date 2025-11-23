pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    environment {
        VERSION = '1.0.0'
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building...'
                echo "Version: ${VERSION}"

                // Maven version check on Windows
                bat 'mvn -version'
            }
        }

        stage('Test') {
            when {
                expression { return env.BRANCH_NAME == 'master' }
            }
            steps {
                echo "Testing only on master branch"
                echo "Version: ${VERSION}"

                // Example Maven test command
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                echo "Deploying version: ${VERSION}"

                // Example deploy placeholder
                bat 'echo Deploy step running...'
            }
        }
    }

    post {
        always {
            echo 'Post build action executed.'
            echo "Pipeline completed for version ${VERSION}"
        }
    }
}
