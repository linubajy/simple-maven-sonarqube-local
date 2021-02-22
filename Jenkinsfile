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
              withSonarQubeEnv('sonarqube') {
                withMaven(maven:'maven') 
                sh 'mvn sonar:sonar'
              }
            }
          }
    }
}
