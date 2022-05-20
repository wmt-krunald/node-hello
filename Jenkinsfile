pipeline {
    agent any
 
    tools {nodejs "node"}

    environment {
        CI = 'true'
    }

    stages{

        stage('check') {
            steps {
            sh 'npm config ls'
            }
        }

        stage('build') {
            steps {
                sh 'npm i'
            }
        }

        stage('start') {
            steps {
                sh 'node index.js'
            }
        }
    }

}