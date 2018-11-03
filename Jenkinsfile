node('sonar_slave') {
   
stage('SCM') 
{
git 'https://github.com/shivakumarmanne/game-of-life.git'
 }
 
stage('SonarQube Scanner')
{
withSonarQubeEnv('Sonar') {
def mvnHome = tool name: 'Maven', type: 'maven'
sh "${mvnHome}/bin/mvn install sonar:sonar"
}
}
}
