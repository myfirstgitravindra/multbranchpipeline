pipeline{
  agent {
        label 'linux1'
    }
  stages{
    stage('git checkout'){
      when {
        branch 'test'
      }
      steps{
        echo 'git checkout done...'
      }
    }
     stage('sonarqube'){
      when {
        branch 'develop'
      }
      steps{
        echo 'static scan done...'
      }
    }
     stage('maven build'){
      when {
        branch 'uat'
      }
      steps{
        echo 'maven buid done...'
      }
    }
     stage('nexus'){
      when {
        branch 'main'
      }
      steps{
        echo 'uploading to nexus artifact  done...'
      }
    }
  }
}
