pipeline{
  agent any
  stages{
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
            sh "mv https://get.jenkins.io/war-stable/latest/jenkins.war target/jenkins.war"
       }
     }
  }
}  
