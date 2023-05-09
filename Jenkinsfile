pipeline {
    agent {
        docker {
            image 'node:16-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CHROME_BIN = '/bin/google-chrome'
    }

    stages {
        stage('Dependencies') {
            steps {
                sh 'npm i'
            }
        }
        stage('Build') {
            steps {
                sh 'node -v'
                sh 'npm run build'
            }
        }
//         stage('Unit Tests') {
//             steps {
//                 sh 'ps -ef | grep Xvfb'
//                 sh 'npm run test'
//             }
//         }
//         stage('e2e Tests') {
//             steps {
//                 sh 'npm run cypress:ci'
//             }
//         }
//         stage('Deploy') {
//             steps {
//                 echo 'Deploying....'
//             }
//         }
    }

//     post {
//         always {
//             junit 'results/cypress-report.xml'
//         }
//     }
}
