pipeline{
    agent{
        docker{
            image 'node:16.14.2'
            args '-p 3000:3000'
        }

    stages{
        stage('build'){
            step{
                sh 'npm install'
            }
        }

        // stage('test'){
        //     step{
                
        //     }
        // }

        // stage('deploy'){
        //     step{
                
        //     }
        // }
    }

    }
}