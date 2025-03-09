pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'echo "Hello, Jenkins!" > /tmp/output.txt'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh 'cat /tmp/output.txt' // Accesses the stashed file
                }
            }
        }
    }
}
