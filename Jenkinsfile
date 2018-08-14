pipeline {
  agent any
  stages {
    stage('Check if File Exists') {
      environment {
        existe = ''
      }
      steps {
        fileExists '\\\\g100603sv078\\Interfaces_STD_Firstdata\\XCOM\\PL122D.*'
        sh '''file = "\\\\\\\\g100603sv078\\\\Interfaces_STD_Firstdata\\\\XCOM\\\\PL122D.$(date +%Y%m%d)
.192"
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