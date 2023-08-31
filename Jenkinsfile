pipeline {
   agent any

tools{nodejs "node"}

   stages {
      stage("build") {
        steps {
          sh 'npm install'
        }
      }

      stage("test") {
        steps {
          sh 'npm install'
         sh 'npm test'
        }
      }

      stage("deploy") {
        steps{
          echo "able to deploy..."
        }
       
      }

   }
}