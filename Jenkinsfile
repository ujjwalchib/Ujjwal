pipeline {
  agent any
  stages {
    stage('version') {
      steps {
	echo 'Stage Version'
        
      }
    }
    stage('hello') {
      steps {
	echo 'Stage Hello'
        sh 'javac Test.java'
	sh 'java Test'
      }
    }
  }
}
