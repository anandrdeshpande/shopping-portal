pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable

    tools{
       nodejs 'nodejs' 
    }
    

    stages{
        stage('build'){
            steps{
                echo 'this is the build job'
                sh 'npm install'
            }
        }

        stage('test'){
            steps{
                echo 'this is the test job'
                sh 'npm test'
            }
        }

        stage('package'){
            steps{
                echo 'this is the package job'
                sh 'npm run package'
            }
        }
        
        stage('Archive'){
            steps{
                echo 'this is the archive job'
                archiveArtifacts '**/distribution/*.zip'
            }
        }
    }
    
    post{
        always{
            echo 'Shopping Portal this pipeline has completed...'
        }
        
    }
    
}
