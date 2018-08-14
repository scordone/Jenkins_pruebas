pipeline {
  agent any
  stages {
    stage('Check if File Exists') {
      environment {
        existe = ''
      }
      steps {
        fileExists '\\\\\\\\g100603sv078\\\\Interfaces_STD_Firstdata\\\\XCOM\\\\PL122D.20180711.192'
        sh '''set echo off
dia="$(date +%Y%m%d)"
dia="20180711"
file="\\\\\\\\g100603sv078\\\\Interfaces_STD_Firstdata\\\\XCOM\\\\PL122D.$dia.192"
if [ -f "$file" ]
then
	echo "$file found."
else
	echo "$file not found."
fi
echo "${test}"'''
      }
    }
  }
  environment {
    test = 'SI'
  }
}