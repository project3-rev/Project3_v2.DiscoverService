pipeline {
   agent any
   stages {
      stage('Compile') {
         steps {
            sh 'mvn clean package'
         }
      }
      stage('Docker') {
         steps {
            sh 'sudo docker build -t sebenner/project_03:discover-service .'
            sh 'sudo docker push sebenner/project_03:discover-service'
            sh 'sudo docker run discover-service'
            sh 'sudo docker image ls'
         }
      }
      /*stage('Deploy') {
         steps {
            sh 'mvn package'
         }
      }*/
   }
}
