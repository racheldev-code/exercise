pipeline{
    agent any
    stages{
        stage('1-git-clone'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-jp', url: 'https://github.com/racheldev-code/exercise.git']]])
            }
        }
        stage('2-cpuinfo'){
            steps{
                sh 'lscpu'
            }
        }
    }
}
