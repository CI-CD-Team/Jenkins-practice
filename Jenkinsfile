pipeline {
   agent any

   stages {
      stage("build") {
        steps {
          echo 'building our app to test...'
        }
      }

      stage("test") {
        steps {
         echo 'testing our app...'
        }
      }

      stage("deploy") {
        when{
          expression {
            currentBuild.result == null || currentBuild.result == 'Success'
          }

        }
        steps {
          sh 'make publish'
        }
      }

   }
}