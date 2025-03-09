pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'echo "Hello, Jenkins!" > output.txt'
                    stash name: 'myFiles', includes: 'output.txt'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    unstash 'myFiles'
                    sh 'cat output.txt' // Accesses the stashed file
                }
            }
        }
    }
}
