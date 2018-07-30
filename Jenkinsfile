node{
  stage('SCM Checkout'){
  git 'https://github.com/itzprashanth/mavenproject'
  }
  stage('Compile package'){
  def mvnHome = tool name: 'Maven', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Email Notification'){
    mail bcc: '', body: 'How are you?', cc: '', from: '', replyTo: '', subject: 'HI', to: 'prashanth.devops6@gmail.com'
  }
}
