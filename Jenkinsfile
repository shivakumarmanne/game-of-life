pipeline{
    agent any
    stages{
        stage ("Maven Build"){
            steps{
                git url: 'https://github.com/shivakumarmanne/game-of-life.git'
                bat '''
                mvn clean install
                '''
            }
        }
    }
}
