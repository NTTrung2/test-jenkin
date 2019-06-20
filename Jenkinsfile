pipeline {
    agent any
	   environment {
		TEST01 = "echo test01"
		TEST02 = "java -version"
    }
    stages {
        stage("environment") {
            steps {
     		sh TEST01
			sh TEST02
            }
        }
    }
}
