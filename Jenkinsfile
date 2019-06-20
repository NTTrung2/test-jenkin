pipeline {
    agent any
  
    parameters {
		choice(choices: ["DEV","PRODUCTION"], description: 'What environment?', name: 'ENVIRONMENT')
    }

    stages {
      
          when {
    			allOf {
    				expression { params.ENVIRONMENT ==~ /DEV/ }
    			}
    		}
    		agent any
    	    stages {
    	        stage("print environment") {
                    steps {
                        script { bat "echo ${params.ENVIRONMENT}" }
                    }
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
