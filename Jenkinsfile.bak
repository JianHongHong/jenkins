pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/JianHongHong/ansible-multipass.git'
      }
    }

    stage('Run Ansible') {
      steps {
        script {
          sh 'ansible-playbook -i inventory provison.yml'
        }
      }
    }
  }
}
