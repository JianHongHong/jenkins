pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/JianHongHong/ansible-multipass.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                // Add build commands here
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Add test commands here
            }
        }
    }
}
