pipeline {
  agent any
    tools {
      python 'python2.7.12'
    }
    stages {
      stage ('Decl Main') {
        steps {
          echo "From the declarative pipeline script"
        }
      }
      stage ('Python Init') {
        steps {
          sh '''
             echo PATH = ${PATH}
          '''
        }
      }
    }
}
