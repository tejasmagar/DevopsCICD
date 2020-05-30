pipeline {
        agent any
            stages  {
              stage ('Upload to AWS'){
                      withAWS(region:'eu-west-1) {
                                                         sh 'echo"Region is EU-WEST"'
                                                  }
                       s3Upload(file:'index.html', bucket:'tejascdci', path:'index.html')
                              
                              steps{
                                sh 'echo "Hello World"'
                                sh'''
                               echo "Multiline shell steps works too"
                                ls -lah
                                 '''
                                    }
                               }
                      }
          }
