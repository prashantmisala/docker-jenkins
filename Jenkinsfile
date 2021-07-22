pipeline {
  agent any
  environment {
      DOCKER = credentials('dockerhub')
       } 
    stages {
       stage('building image') {
          steps {
            sh 'docker build -t prashant1311/jen:latest .'
		}
            }
       stage('login') {
         steps {
           sh 'docker login $DOCKER'
             }
          }
       stage('push') {
         steps {
           sh 'docker push prashant1311/jen:latest'
             }
          }    
       stage('running') {
          steps {
           sh 'docker run -dt --name=c3 prashant1311/jen:latest'  
             }
         }
      }
  }     
