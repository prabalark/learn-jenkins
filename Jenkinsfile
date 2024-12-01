pipeline{

  agent {
     node {
       label 'terraform-workstation' # have to give instance name
   }
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