pipeline {
    agent any
    tools {nodejs "nodejs"}
    stages {
        stage("Install") {
            steps {
                bat "npm -v"
            }
        }
    }
}
