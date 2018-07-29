pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'python Test.py'
      }
    }
    stage('Compile') {
      parallel {
        stage('Compile') {
          steps {
            sh 'python Compile.py'
          }
        }
        stage('') {
          steps {
            mail(subject: 'Test Completed', body: 'Test for job AnntinuJenkins completed', from: 'anntinutj@gmail.com', to: 'anntinumets@gmail.com')
          }
        }
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