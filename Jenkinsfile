pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/zenitsua2416/jenkins-test.git'
            }
        }

        stage('Run files') {
            steps {
                sh 'node run.js'
            }
        }
    }

    post {
        success {
            echo 'Build successful'
        }
        failure {
            echo 'Build failed!!'
        }
    }
}
