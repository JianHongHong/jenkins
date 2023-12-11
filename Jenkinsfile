pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Replace 'your-repo-url' with your Git repository URL
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], 
                          userRemoteConfigs: [[url: 'https://github.com/JianHongHong/ansible-multipass.git']]])
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
