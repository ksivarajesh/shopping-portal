pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejssrk'
    }
    

    stages{
        stage('compile'){
            steps{
                echo 'this is the Compile job'
                sh 'npm install'
            }
        }
        stage('test'){
            steps{
                echo 'this is the Test job'
		sh 'npm test'
            }
        }
        stage('package'){
            steps{
                echo 'this is the Package job'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'this AUTOMATED PIPELINE has completed SUCCESSFULLY...'
        }
        
    }
    
}
