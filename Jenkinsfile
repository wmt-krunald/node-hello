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

        stage('strat') {
            steps {
                sh 'node index.js'
            }
        }

        // stage('deploy') {
        //     environment {
        //         NETLIFY_AUTH_TOKEN = credentials('NETLIFY_AUTH_TOKEN')
        //         NETLIFY_SITE_ID = credentials('NETLIFY_SITE_ID')
        //     }
            
        //     steps {
        //         sh 'npm install netlify-cli'
        //         sh 'npx netlify deploy --site $NETLIFY_SITE_ID --auth $NETLIFY_AUTH_TOKEN --dir build/ --prod'
        //     }
        // }
    }

}