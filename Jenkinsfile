node{
    
        stage("Checkout"){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/gopalaa/docker-react-test.git']]])
            }
           
        }
        
        stage("Build Docker Image"){
            steps{
                script{
                    sh 'docker build -t venuduggyala/docker-react-test -f Dockerfile.dev .'
            }
        }
    }
    stage("Run Tests"){
            steps{
                script{
                    sh 'docker run -e CI=true venuduggyala/docker-react-test npm run test'
            }
        }
    }

}