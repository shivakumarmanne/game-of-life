
node('sonar_slave') {
   
stage('SCM') {

git 'https://github.com/shivakumarmanne/game-of-life.git'

   }
 
Stage('SonarQube Scanner')
{
withSonarQubeEnv('Sonar') {
Sh 'mvn install sonar:sonar   
}

}

}
