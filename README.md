pipeline {
    agent any

    stages {
        stage('Creating') {
            steps {
                bat 'echo Hello World>file1.txt'
            }
        }
        stage('Copy') {
            steps {
                bat 'copy file1.txt file2.txt'
            }
        }
        stage('Display') {
            steps {
                bat 'type file2.txt'
            }
        }
    }
}
