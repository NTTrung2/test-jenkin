pipeline {
    agent any
    parameters {
		choice(choices: ["DEV","PRODUCTION"], description: 'What environment?', name: 'ENVIRONMENT')
    }
    stages {
        stage("condition dev") {
		    when {
    			allOf {
    				expression { params.ENVIRONMENT ==~ /DEV/ }
    			}
    		}
    		agent any
    	    stages {
    	        stage("print environment") {
                    steps {
                        script { sh "echo ${params.ENVIRONMENT}" }
                    }
    	        }
            }
	    }
        stage("condition prod") {
		    when {
    			allOf {
    				expression { params.ENVIRONMENT ==~ /PRODUCTION/ }
    			}
    		}
    		agent any
    	    stages {
    	        stage("print environment") {
                    steps {
                        script { sh "echo ${params.ENVIRONMENT}" }
                    }
    	        }
            }
	    }
    }
}
