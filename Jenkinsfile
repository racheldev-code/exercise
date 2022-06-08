pipeline{
    agent any
    stages{
        stage('1-firststage'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-jp', url: 'https://github.com/racheldev-code/exercise.git']]])
            }
        }
        stage('2-systemcheck'){
            steps{
                sh 'free -g'
            }
        }
    }
}