pipeline{

  agent {
     node {
       label 'terraform-workstation'
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