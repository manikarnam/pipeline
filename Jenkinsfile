currentBuild.displayName="ManiDeclarativepipeline-#"+currentBuild.number
pipeline {
    agent none
     stages {
         stage('Database') {
            agent {
                docker {image 'redis'}
            }
             steps{
              echo 'succsessfully image builded'
             }
         }

         stage('hello-world'){
             agent {
                 docker {image 'alpine'}
             }
         
             steps {
                 echo 'successfully build image'
             }
         }
     
         stage('openjdk'){
             agent {
                 docker {image 'openjdk'}
            
            }
         steps{
             echo 'Successfully build the image'
            }
             
         }
     
         stage('registry'){
             agent {
                 docker {image 'registry'}
             }
         steps{
             echo "successfully build"
         }
             
         }
     
         stage('maniengg'){
             agent {
                 docker {image 'maniengg/golangrest-api'}
             }
        steps{
            echo 'successfully execute'
        }
  }
   
    stage('Deploy to prod server'){
        agent{
            docker {image 'centos'}
        }
            steps{
                echo "successfully"
         
        }
    
    }
   
     }
}
