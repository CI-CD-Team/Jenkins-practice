pipeline {
   agent {
    docker{
      image 'node:6-alpine'
            args '-p 3000:3000'
    }
   }
   environment{
    CI = 'true'
   }

   stages {
      stage("build") {
        steps {
          sh 'npm install'
        }
      }

      stage("test") {
        steps {
         sh 'npm run test'
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