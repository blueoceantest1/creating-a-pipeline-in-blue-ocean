pipeline {
  agent {
    docker {
      image 's.docker-registry.corp.changers.team/balance-admin-client'
      args '-p 8082:80/tcp'
    }
    
  }
  stages {
    stage('build') {
      steps {
        git(url: 'git@github.com:jenkins-docs/creating-a-pipeline-in-blue-ocean.git', branch: 'master')
        sh 'yarn && yarn tsc'
      }
    }
  }
}