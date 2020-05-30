pipeline {
        agent any
            stages  {
              stage ('Upload to AWS'){                     
                              steps{
                                sh 'echo "Hello World"'
                                sh'''
                               echo "Multiline shell steps works too"
                                ls -lah
                                 '''
                                    }
                               }
                    withAWS(region:'eu-east-1') {
                                                         sh 'echo"Region is EU-EAST"'
                       s3Upload(file:'index.html', bucket:'tejascdci', path:'index.html')
                      }
          }
