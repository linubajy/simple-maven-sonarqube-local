pipeline{
  agent any
  tools
  {
    maven 'maven'
    jdk 'JDK'
  }
       
  stages {
          stage("build & SonarQube analysis") {
            agent any
            steps {
              withSonarQubeEnv('sonarlocal') 
              {
                  sh 'java -version'
                   sh 'mvn clean package sonar:sonar'
              }
             
            }
          }
    }
}



