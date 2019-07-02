pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Check version') {
            steps {
                bat 'npm -v'
            }
        }
        stage('Install Library') {
            steps {
                bat 'npm install'
            }
        }
        stage('Build source') {
            steps {
                bat 'npm run build'
            }
        }
    }
}
