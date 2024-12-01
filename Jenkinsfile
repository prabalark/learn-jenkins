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
     string(name: 'PERSON', defaultValue: 'Mr prabala', description: 'Who should I say hello to?')
  }

  stages {
     stage('one') {
       input {
         message "Should we continue?"
         ok "Yes, we should."
       }
       steps {
         sh 'echo Hello World'
         sh 'echo Hello universe'
         sh 'echo ${sample}'
         sh 'echo name - ${PERSON}'
       }

     stage('two') {
       steps {
         sh 'env'
       }

      }
     }
  }

  post {
     always {
       sh 'echo post cleanup steps'
     }
  }

}

