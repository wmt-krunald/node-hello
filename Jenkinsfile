// pipeline {
//     agent any 
// //     {
// //         docker {
// //             image 'node:16.14.2'
// //         }
// //     }

//     environment {
//         CI = 'true'
//     }

//     stages{
        
//         stage('build') {
//             steps {
//                 sh 'npm ci'
//                 sh 'npm run build'
//             }
//         }

//         // stage('test'){
//         //     steps {
//         //         sh 'npm run test'
//         //     }
//         // }

// //         stage('deploy'){
// //             steps {             
                
// //             }
// //         }
//     }

// }
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
                sh 'npm run build'
            }
        }

        stage('start') {
            steps {
                sh 'npm run start'
            }
        }
        stage('deploy') {
            environment {
                NETLIFY_AUTH_TOKEN = credentials('NETLIFY_AUTH_TOKEN')
                NETLIFY_SITE_ID = credentials('NETLIFY_SITE_ID')
            }
            
            steps {
                sh 'npm install netlify-cli'
                sh 'npx netlify deploy --site $NETLIFY_SITE_ID --auth $NETLIFY_AUTH_TOKEN --dir build/ --prod'
            }
        }
    }

}