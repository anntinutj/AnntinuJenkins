pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'python Test.py'
      }
    }
    stage('Compile') {
      steps {
        sh 'python Compile.py'
      }
    }
    stage('Build') {
      steps {
        sh 'python Build.py'
      }
    }
    stage('Deployment') {
      steps {
        sh 'python Deploy.py'
      }
    }
  }
}