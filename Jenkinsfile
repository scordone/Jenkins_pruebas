pipeline {
  agent any
  stages {
    stage('Check if File Exists') {
      environment {
        existe = 'YES'
      }
      steps {
        fileExists '\\\\g100603sv078\\Interfaces_STD_Firstdata\\XCOM\\PL122D.*'
      }
    }
    stage('') {
      steps {
        echo 'existe'
      }
    }
  }
}