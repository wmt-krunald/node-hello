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
            }
        }

        stage('start') {
            steps {
                sh 'node index.js'
            }
        }
    }

}