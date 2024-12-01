pipeline{

  agent {
     node {
       label 'terraform-workstation'
   }
  }

  options {
    ansiColor('xterm')
  }

  stages {

     stage('one') {
       steps {
         sh 'echo Hello World'
         sh 'echo Hello universe'
       }
     }
  }

}