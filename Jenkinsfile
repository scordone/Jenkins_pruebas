pipeline {
  agent any
  stages {
    stage('Check if File Exists') {
      environment {
        existe = ''
      }
      steps {
        fileExists 'jenkinsfile'
        sh '''set echo off
dia="$(date +%Y%m%d)"
dia="20180711"
prueba="a"
file="\\\\\\\\g100603sv078\\\\Interfaces_STD_Firstdata\\\\XCOM\\\\PL122D.$dia.192"
if [ -f "$file" ]
then
        prueba="ENCONTRE"
        test="ENCONTRE"
        set test
	echo "$file found."
else
        prueba="NO LO ENCONTRE"
	echo "$file not found."
fi
echo "${test}"'''
      }
    }
    stage('FIN') {
      steps {
        sh 'echo "${test}"'
      }
    }
  }
  environment {
    test = 'SI'
  }
}