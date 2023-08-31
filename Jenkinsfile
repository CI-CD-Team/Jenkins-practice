pipeline {
   agent any
   
   tools {nodejs "node"}
  

   stages {
      stage("build") {
        steps {
          sh 'npm install'
        }
      }

      stage("test") {
        steps {
         echo "no test implemented.."
        }
      }

      stage("deploy") {
        steps {
         echo 'App is ready to deploy..'
        }
      }

   }
}