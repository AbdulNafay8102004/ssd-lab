pipeline {
    agent any

    environment {
        VERSION = '1.0.0'
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building...'
                echo "Version: ${VERSION}"
            }
        }

        stage('Test') {
            when {
                expression { return env.BRANCH_NAME == 'master' }
            }
            steps {
                echo "Testing only on master branch"
                echo "Version: ${VERSION}"
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                echo "Deploying version: ${VERSION}"
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
