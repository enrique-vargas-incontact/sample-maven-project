pipeline {
    agent any 
    tools {
	  maven 'Maven3'
	  jdk 'jdk-17'
	}
    stages {
      stage('Initialize') {
        steps {
        echo 'Maven version..'
	    bat "mvn -version"
      }
    }    
    stage('Build') {
      steps {

        bat 'mvn clean install'

      }
      post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
      }	    
    }

  }
}
