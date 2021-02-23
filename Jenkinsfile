pipeline{
  agent any
  tools
  {
    maven 'maven'
    jdk 'JDK'
  }
       
  stages {
          stage("build & SonarQube analysis") {
            steps {
              withSonarQubeEnv('sonarlocal') 
              {
                  bat 'java -version'
                  bat 'mvn sonar:sonar'
              }
             
            }
          }
    }
}



