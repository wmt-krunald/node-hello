pipeline {
    agent any 
//     {
//         docker {
//             image 'node:16.14.2'
//         }
//     }

    environment {
        CI = 'true'
    }

    stages{
        
        stage('build') {
            steps {
                sh 'npm ci'
                sh 'npm run build'
            }
        }

        // stage('test'){
        //     steps {
        //         sh 'npm run test'
        //     }
        // }

//         stage('deploy'){
//             steps {             
                
//             }
//         }
    }

}
