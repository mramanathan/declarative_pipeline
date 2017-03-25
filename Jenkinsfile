pipeline {

  agent any
  stages {
    stage ('Env vars...') {
      steps {
        sh 'printenv'
      }
    }
  }

  agent {
  // tools {
    // Valid tool types: [ant, hudson.tasks.Ant$AntInstallation, org.jenkinsci.plugins.docker.commons.tools.DockerTool, 
    // git, hudson.plugins.git.GitTool, gradle, hudson.plugins.gradle.GradleInstallation, jdk, hudson.model.JDK, jgit, 
    // org.jenkinsci.plugins.gitclient.JGitTool, jgitapache, org.jenkinsci.plugins.gitclient.JGitApacheTool, maven, hudson.tasks.Maven$MavenInstallation
    // python 'python2.7.12'
    // git 'Default'
  // }
    docker {
      image 'golang:1.6'
    }
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
           echo "PATH = ${PATH}"
        '''
      }
      post {
        always {
          echo "Message from post internal to steps and stage"
        }
      }
    }
  }

  post {
    always {
      echo "External post saying echo"
    }
  }
}
