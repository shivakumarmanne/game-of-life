pipeline{
    agent any
    options { timestamps() }
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
    post{
        success{
            archiveArtifacts 'gameoflife-web/target/*.war'
        }
    }
}
