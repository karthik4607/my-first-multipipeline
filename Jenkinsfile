

pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('cat Readme') {
           when{
             branch 'test'
            }
   	   steps {
             sh'cat 'readme' '
                   }
        }
    }
}
