pipeline{ 
      agent { docker 'ubuntumaven:1.0' }
      stages{
      stage('build'){
                  steps{
                  sh "rm -rf hello-world-war"
                  sh "git clone https://github.com/sandy1791994/hello-world-war.git"
                  sh "mvn clean package"
                  }
                  }
      }
      }
      

      
