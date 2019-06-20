pipeline {
    agent any
	   environment {
		TEST01 = "echo test01"
		TEST03 = "java -version"
    }
    stages {
        stage("environment") {
            steps {
     		sh TEST01
			sh TEST03
            }
        }
    }
}

