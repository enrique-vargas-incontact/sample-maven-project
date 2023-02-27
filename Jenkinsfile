pipeline {
    agent any 
    tools {
	  maven 'Maven3'
	  jdk 'jdk-17'
	}
    stages {
      stage('Load Tools') {
        steps {
        echo 'Loading Tools..'
	    bat "mvn -version"
      }
    }    
    stage('maven install') {
      steps {

        bat 'mvn clean install'

      }
    }

  }
}
