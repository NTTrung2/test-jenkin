pipeline {
    agent any
    stages {
        stage("Check version npm") {
            steps {
                bat "npm -v"
            }
        }
        stage("Check version node") {
            steps {
                bat "node -v"
            }
        }
        stage("Install lib") {
            steps {
                bat "npm install"
            }
        }
        stage("build") {
            steps {
                bat "npm run build"
            }
        }
    }
}
