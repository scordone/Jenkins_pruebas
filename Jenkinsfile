pipeline {
  agent any
  stages {
    stage('Check if File Exists') {
      steps {
        fileExists '\\\\g100603sv078\\Interfaces_STD_Firstdata\\XCOM\\PL122D.*'
        sh '''bat \'set > env.txt\' 
for (String i : readFile(\'env.txt\').split("\\r?\\n")) {
     println i
}'''
      }
    }
  }
}