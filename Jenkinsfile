pipeline{
    agent any
    tools{
        jdk "JDK"
        maven "maven"
    }
    stages{
        stage ("Updated Stage Maven"){
            steps{
                git url: 'https://github.com/shivakumarmanne/game-of-life.git'
                sh '''
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
