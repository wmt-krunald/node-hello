pipeline {
    agent any 

    environment {
        CI = 'true'
    }

    stages{
        
        stage('build') {
            steps {
                sh 'npm i'
                sh 'npm run build'
            }
        }
    }

}