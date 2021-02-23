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
              withSonarQubeEnv('sonar-server') 
              {
                withMaven(maven:'maven')
                {
                  bat 'java -version'
                  bat 'mvn sonar:sonar'
              }
              }
            }
          }
    }
}



