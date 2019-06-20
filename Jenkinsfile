pipeline {
    agent any
    tools {nodejs "nodejs"}
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
        stage("Check version angular") {
            steps {
                bat "ng version"
            }
        }
    }
}
