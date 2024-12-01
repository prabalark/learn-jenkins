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
     stage('parallel') {
       parallel {
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
         }
         stage('Two') {
           when {
             expression {
               GIT_BRANCH == "origin/test"
             }
           }
           steps {
             sh 'env'
           }
         }
         stage('Three') {
           when {
             expression {
               GIT_BRANCH == "origin/main"
             }
           }
           steps {
             sh 'echo hello'
           }
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

