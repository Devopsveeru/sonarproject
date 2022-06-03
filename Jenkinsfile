pipeline{
  agent any
  stages{
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
        }
     }
     stage('Sonar_test') {
       steps{
           withSonarQubeEnv('My SonarQube Server') { // If you have configured more than one global server connection, you can specify its name
           sh "${scannerHome}/bin/sonar-scanner"
           }    
        }
     }
    } 
}            
