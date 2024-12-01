pipeline {

  agent {
     node {
       label 'terraform-workstation'
   }
  }

  environment {
     sample = "example.com"
  }

  parameters {
     string(name: 'name', defaultValue: 'Mr prabala', description: 'Who should I say hello to?')
  }

  stages {

     stage('one') {
       steps {
         sh 'echo Hello World'
         sh 'echo Hello universe'
         sh 'echo ${sample}'
         sh 'echo name - ${name}'
       }
     }
  }

  post {
     always {
       sh 'echo post cleanup steps'
     }
  }

}

