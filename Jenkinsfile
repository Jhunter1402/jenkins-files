pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from Git
                checkout scm
            }
        }
        stage('Installation') {
            steps {
                // Use double quotes for consistency
                sh "sudo yum install epel-release -y"
                sh "sudo yum install ansible -y"
            }
        }
        stage('Install-Services') {
            steps {
                // Use double quotes for consistency
                sh "ansible-playbook install_services.yml"
            }
        }
    }
}
