pipeline {
  agent any
  environment {
      DOCKER = credentials('dockerhub')
       } 
    stages {
       stage('building image') {
          steps {
            sh 'docker build -t c1 .'
		}
            }
       stage('login') {
         steps {
           sh 'docker login -u $DOCKER'
             }
          }
       stage('running') {
          steps {
           sh 'docker run -dt --name=c2 c1'  
             }
         }
      }
  }     
