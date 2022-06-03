pipeline{
  agent any
  stages{
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
            sh "mv https://get.jenkins.io/jar-stable/latest/jenkins.jar target/jenkins.jar"
       }
     }
  }
}  
