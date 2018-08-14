pipeline {
  agent any
  stages {
    stage('Check if File Exists') {
      environment {
        existe = ''
      }
      steps {
        fileExists '\\\\g100603sv078\\Interfaces_STD_Firstdata\\XCOM\\PL122D.*'
      }
    }
    stage('pipe') {
      steps {
        script {
          pipeline {
            agent any

            environment {
              DISABLE_AUTH = 'true'
              DB_ENGINE    = 'sqlite'
            }

            stages {
              stage('Build') {
                steps {
                  sh 'printenv'
                }
              }
            }
          }
        }

      }
    }
  }
}