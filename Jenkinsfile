node{
    stage('Clone repository') {
    git 'https://github.com/khallouli-dorra/AnsibleDocker-Freedomtravel.git'    
    }
     
    stage('deploy my app docker') {
        sh """
        ansible-playbook deploy_freedomtravel.yml -i hosts.ini -u ansible
        """
        }       
    }
