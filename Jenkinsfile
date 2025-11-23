pipeline {
    agent any
    tools {
        jdk 'JDK17'      // must match the name you set in Jenkins
        maven 'Maven'    // must match Maven tool name
    }
    environment {
        PATH = "${tool 'Maven'}\\bin;${env.PATH}"
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn -version'
                bat 'mvn clean install'
            }
        }
    }
}
