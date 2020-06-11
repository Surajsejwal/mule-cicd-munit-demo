pipeline {
  agent any
  stages {
    stage('Build Application') { 
      steps {
        bat 'mvn -B -U -e -V clean -DskipTests install'
      }
    }
    
 	stage('Test') { 
      steps {
        echo 'Test Appplication...' 
        bat 'mvn test'
      }
    }
	stage('Deploy CloudHub') { 
       steps {
        echo "Deploying only because of code commit..."
        bat 'mvn package deploy -DmuleDeploy'
      }
    }
  }
}
