pipeline{

  agent {
     node {
       label 'terraform-workstation'
   }
  }

  options {
    ansicolor('xterm')
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