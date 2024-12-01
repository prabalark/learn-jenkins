pipeline{

  agent {
     node {
       label 'terraform-workstation' # have to give instance name
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