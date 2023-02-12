pipeline {
  agent any
  tools {
    maven "maven"
  }
  stages {
    stage ('Maven clean') {
      steps {
      sh 'mvn clean'
      }
  
    }
    
    stage ("Maven build") {
      steps {
      sh 'mvn package'
      }
    
    } 
    
    stage ('Docker build') {
      steps {
      
      sh 'docker build -t devopstrainingschool/jenkins-java-maven .'
      
      }
    
    
    
    }
   
    
    
    
    
    
    
    
  }
  
  













}
