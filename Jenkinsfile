pipeline{
      agent { label 'salve1' }
      stages{
      stage('check out'){
                  steps{
                  sh "git clone https://github.com/sandy1791994/hello-world-war.git"
                  }
                  }
      stage('build'){
      steps{
      sh "mvn package"
      }
      }
      }
      }
