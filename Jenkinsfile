pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Test') {
            when {
                expression { return env.BRANCH_NAME == 'master' }
            }
            steps {
                echo "Testing only on master branch"
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        always {
            echo 'Post build action executed.'
        }
    }
}
