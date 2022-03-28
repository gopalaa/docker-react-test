pipeline{
    agent{
        dokcer{
            image 'node:6-alpine'
            args '-p 3000:300'
        }
    }
    stages{
        stage('Build'){
            steps{
                sh 'npm install'
            }
        }
    }
}