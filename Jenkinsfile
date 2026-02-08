pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {

                git branch: 'main',
                    url: 'https://github.com/adhilakshm/devops_practise.git'
            }
        }
        stage('Run'){
            steps{
                sh 'ssh -o StrictHostKeyChecking=no -i /keys/target_key.pem ec2-user@3.141.18.251 "hostname"'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                    sh 'ansible-playbook playbooks/disk.yaml -i inventory'
                }
            }
        }
    }

