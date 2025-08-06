pipeline {
  agent any

  stages {
    stage('Checkout') {
        steps {
            git ''
        }
    }

    stage('Build') {
      steps {
        sh '''
          kubectl apply -f .
        '''
      }
    }
  }

  post {
    always {
      echo "Pipeline Finished"
    }

    success {
      echo "Pipeline Successful!"
    }

    failure {
      echo "Pipeline Failed!"
    }
  }
}