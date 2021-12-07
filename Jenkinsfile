pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        echo 'this is the Compile job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the Test job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the Package job'
        sh 'npm run package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejssrk'
  }
  post {
    always {
      echo 'this AUTOMATED PIPELINE has completed SUCCESSFULLY...'
    }

  }
}