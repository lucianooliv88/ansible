pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/lucianooliv88/ansible'
            }
        }
        stage('Running Ansible'){
            steps{
                ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts.inv', playbook: 'installing-httpd.yml'
            }
        }
    }
}
