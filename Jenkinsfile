pipeline {
    agent any
    parameters {
		choice(choices: ["DEV","TEST","PRODUCTION"], description: 'What environment?', name: 'ENVIRONMENT')
    }
    stages {
        stage("parameters") {
            steps {
                script {
                    sh "echo ${params.ENVIRONMENT}"
                }
            }
        }
    }
}
