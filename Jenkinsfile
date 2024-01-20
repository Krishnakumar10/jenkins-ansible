 pipeline{

 agent any

 stages{

 stage('Checkout'){
  steps{
       git branch: 'main', credentialsId: '5e588bcf-9e01-4855-a376-d83651e7e8f8', url: 'https://github.com/Krishnakumar10/jenkins-ansible.git'
       }
 }
 stage('AnsibleExecution'){
  steps{
    ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dhost.inv', playbook: 'apache.yml', vaultTmpPath: ''
      }
    }
}
}
