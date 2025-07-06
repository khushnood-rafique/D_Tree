pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                cleanWs()
                echo 'Building a new laptop...'
                sh 'mkdir -p build'
                sh 'touch build/computer.txt'
                sh 'echo "mainboard" >> build/computer.txt'
                sh 'cat build/computer.txt'
                sh 'echo "display" >> build/computer.txt'
                sh 'cat build/computer.txt'
                sh 'echo "keyboard" >> build/computer.txt'
                sh 'cat build/computer.txt'
            }
        }
    }
    
    post {
        success{
            archiveArtifacts artifacts: 'build/**'
        }
    }
}