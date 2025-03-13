pipeline {
  agent any
  stages {
    stage('Build')
      steps {
        build 'PES1UG22CS320-1'
        sh 'g++ cs320.cpp -o cs320'
      }

    }
    stage('Test'){
      steps {
        sh './cs320'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deployed'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
