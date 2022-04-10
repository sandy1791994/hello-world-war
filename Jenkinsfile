pipeline{
      agent { label 'slave1' }
      stages{
      stage('check out'){
                  steps{
                  sh "git pull https://github.com/sandy1791994/hello-world-war.git"
                  }
                  }
      stage('build'){
      steps{
      sh "mvn package"
      }
      }
            stage('docker image build'){
                  steps{
                        sh "docker build -t sandy1791994/docwarimage:1.0 ."
                  }
            }
            stage('docker image push'){
                  steps{
                        sh "docker login -u sandy1791994 -p mAnj@0606g"
                        sh "docker push sandy1791994/docwarimage:1.0"
                  }
            }
            stage('deploy'){
                  agent { label 'slave2' }
                  steps{
                        sh "docker run -d -p  sandy1791994/docwarimage:1.0"
                  }
            }
      }
      }
