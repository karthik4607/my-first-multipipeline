

pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'sudo apt install npm'
            }
        }
        stage('Test') {
            steps {
                sh 'cd docker'
                sh ' sudo ./script.sh'
            }
        }
    }
}
