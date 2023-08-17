pipeline {
    agent any

    stages {
        stage('Testing connection VM2') {
            steps {
                echo 'Start of Ansible ping'
                sh "ansible -m ping all"
                echo 'End of Ansible ping'
            }
        }
        stage('Update ivan-nelub-testVM') {
            steps {
                echo 'Start of Update ivan-nelub-testVM'
                sh "sudo apt update&&apt upgrade -y"
                echo 'End of Update ivan-nelub-testVM'
            }
        }
         stage('Update ivan-nelub-testVM2') {
            steps {
                echo 'Start of Update ivan-nelub-testVM2'
                sh "ansible-playbook playbook-update-VM2.yml"
                echo 'End of Update ivan-nelub-testVM2'
            }
        }
    }
}

