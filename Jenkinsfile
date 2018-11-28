node {
    stage 'Terraform plan'
       ansiColor('xterm') {
        ansibleTower credential: '', extraVars: '', importTowerLogs: true, importWorkflowChildLogs: false, inventory: '', jobTags: '', jobTemplate: 'provision-aws-resources-terraform-plan', jobType: 'run', limit: '', removeColor: false, skipJobTags: '', templateType: 'job', towerServer: 'AnsibleTower-CLI', verbose: false
        }
    stage 'Approval'
       def deploy_validation = input(
            id: 'Deploy',
            message: 'Let\'s continue the deploy terraform plan',
            type: "boolean")

    stage 'Terraform apply'
       ansiColor('xterm') {
        ansibleTower credential: '', extraVars: '', importTowerLogs: true, importWorkflowChildLogs: false, inventory: '', jobTags: '', jobTemplate: 'provision-aws-resources-terraform-apply', jobType: 'run', limit: '', removeColor: false, skipJobTags: '', templateType: 'job', towerServer: 'AnsibleTower-CLI', verbose: false
        }
    stage 'Configuring applications using Ansible'
       ansiColor('xterm') {
        ansibleTower credential: '', extraVars: '', importTowerLogs: true, importWorkflowChildLogs: false, inventory: '', jobTags: '', jobTemplate: 'configure-aws-resources-execute', jobType: 'run', limit: '', removeColor: false, skipJobTags: '', templateType: 'job', towerServer: 'AnsibleTower-CLI', verbose: false
        }
}