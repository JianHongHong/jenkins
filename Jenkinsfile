pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], 
                          userRemoteConfigs: [[url: 'https://github.com/JianHongHong/wagtail-test']]])
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                // Install Poetry
                sh 'curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -'
                // Add Poetry to PATH (assuming bash shell)
                sh 'source $HOME/.poetry/env'
                // Install dependencies using Poetry
                sh 'poetry install'
                // Navigate to 'mysite' directory
                dir('mysite') {
                    // Run Django server
                    sh 'python manage.py runserver'
                }
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
