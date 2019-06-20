pipeline {
    agent any
  
    parameters {
		choice(choices: ["DEV","PRODUCTION"], description: 'What environment?', name: 'ENVIRONMENT')
    }

    stages {
      
      stage("parameters") {
            steps {
                script {
                    sh "echo ${params.ENVIRONMENT}"
                }
            }
        }

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
