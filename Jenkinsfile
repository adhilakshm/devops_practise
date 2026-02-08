pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {

                git branch: 'main',
                    url: 'https://github.com/adhilakshm/devops_practise.git'
            }
        }
     
        stage('Run Ansible Playbook') {
            steps {
                    sh 'ansible-playbook playbooks/disk.yaml -i inventory'
                }
            }
        }
    }

