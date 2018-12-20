node{
  stage('SCM Checkout'){
  git 'https://github.com/itzprashanth/mavenproject'
  }
  stage('Compile package'){
  def mvnHome = tool name: 'Maven', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('SonarQube analysis Ya') {
    withSonarQubeEnv('sonar') {
      def mvnHome = tool name: 'Maven', type: 'maven'
      // requires SonarQube Scanner for Maven 3.2+ 
      sh "${mvnHome}/bin/mvn sonar:sonar"
    }
    }
}
