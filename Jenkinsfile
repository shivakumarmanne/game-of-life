pipeline{
    agent any
    tools{
        jdk "JDK"
        maven "maven"
    }
    stages{
        stage ("Maven-with different version"){
            steps{
                git url: 'https://github.com/shivakumarmanne/game-of-life.git'
                sh '''
                mvn clean install -Dv=${BUILD_NUMBER}
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
