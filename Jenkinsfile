pipeline {
   agent any

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
        steps{
          echo "able to deploy..."
        }
       
      }

   }
}