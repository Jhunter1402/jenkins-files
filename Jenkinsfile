pipeline {
    agent any
    stages {
        stage('Installation') {
            steps {
                // Use double quotes for consistency
                sh "sudo yum install epel-release -y"
                sh "sudo yum install ansible -y"
            }
        }
        stage('Git') {
            steps {
                // Use double quotes for consistency
                git "https://github.com/Jhunter1402/jenkins-files.git"
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
