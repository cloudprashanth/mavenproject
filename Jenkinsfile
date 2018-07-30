node{
  stage('SCM Checkout'){
  git 'https://github.com/itzprashanth/mavenproject'
  }
  stage('Compile package'){
  def mvnHome = tool name: 'Maven', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
}
