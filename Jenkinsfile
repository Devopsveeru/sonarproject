pipeline{
  agent any
  stages{
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
        }
     }
     stage('sonar_test') {
       steps{
           withSonarQubeEnv('SonarQube') { // If you have configured more than one global server connection, you can specify its name
           sh"${scannerHome}/bin/sonar-sacnner"  
           sh "mvn sonar:sonar"
           }    
        }
     }
    } 
}            
