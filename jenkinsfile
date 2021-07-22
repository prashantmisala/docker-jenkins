pipeline {
  agent any
    stages {
       stage('building image') {
          steps {
            sh 'docker build -t c1 .'
		}
            }
       stage('running') {
          steps {
           sh 'docker run -dt --name=c2 c1'  
             }
         }
      }
  }     
