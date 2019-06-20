pipeline {
    agent any
    tools {nodejs "nodejs"}
    stages {
        stage("Install") {
            steps {
                bat label: 'install', script: 'npm -v'
            }
        }
    }
}
