pipeline {
  agent any
  stages {
    stage('Build Application') { 
      steps {
        bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }
    
 	stage('Test') { 
      steps {
        echo 'Test Appplication...' 
        bat 'mvn test'
      }
    }
  }
}
