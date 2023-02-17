pipeline {
    agent any
    stages {
      stage('Build') {
          steps {
              sh 'g++ -o myProgram PES1UG20CS292.cpp'
              build job: 'PES1UG20CS292-1'
          }
      }
      stage('Test') {
          steps {
                sh './myProgram'     //  error should've been `sh './:' `
          }
      }
      stage('Deploy') {
          steps {
              echo 'deployment successful'
          }
      }
  }

  post {
      failure {
          echo 'Pipeline failed'
      }
  }
}
