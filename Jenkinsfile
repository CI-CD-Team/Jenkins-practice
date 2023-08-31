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
          echo "ready to test..."
        }
      }

      stage("deploy") {
        steps{
          echo "able to deploy..."
        }
       
      }

   }
}