

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

        stage('cat Readme') {
           when{
             branch 'test'
           }
            steps{
                sh ''' cat README '''
            }
          } 
          stage('Test') {
            steps {
                sh 'cd docker'
                sh ' chmod +x ./docker/script.sh && ./docker/script.sh'
              }
         }
     }
   }
}
