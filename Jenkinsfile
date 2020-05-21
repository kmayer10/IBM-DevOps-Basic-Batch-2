pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
            echo 'Hello World'
            echo 'This is for Biren Query'
         }
      }
      stage('Maven Build') {
         steps {
            withMaven(maven: 'mvn_3.6.3') {
                sh 'mvn clean package'
            }
            archiveArtifacts 'target/devops.war'
         }
      }
   }
}
