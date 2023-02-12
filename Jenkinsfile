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
    
    stage ("Maven package") {
      steps {
      sh 'mvn package'
      }
    
    } 
    
    stage ('Docker build') {
      steps {
      
      sh 'docker build -t devopstrainingschool/jenkins-java-maven .'
      
      }   
    }
   
    stage ('Docker login and push') {
      steps {
        withDockerRegistry([ credentialsId: "Docker_hub", url: "https://index.docker.io/v1/" ]) {
          sh 'docker push devopstrainingschool/jenkins-java-maven'
        }
      }
    }
    
    
    
    
    
    
  }
  
  













}
