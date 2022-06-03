pipeline{
  agent any
  stages{
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
        }
     }
  stage('Sonar_test') {
    withSonarQubeEnv(credentialsId: 'd8b92de421965020ec3a1192b6601c3abc2efefe', installationName: 'sonar_test') { // You can override the credential to be used
      sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
      }
    }
    }
}        
