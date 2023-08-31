pipeline {
   agent 
   
tools{nodejs "node"}

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