pipeline {
    agent any
    tools {nodejs "NodeJs 10.16.0"}
stages {
        stage('Check version') {
            steps {
                sh 'npm --version'
            }
        }
    }
}


// pipeline {
//     agent { docker { image 'node:6.3' } }
//     stages {
//         stage('build') {
//             steps {
//                 sh 'npm --version'
//             }
//         }
//     }
// }
