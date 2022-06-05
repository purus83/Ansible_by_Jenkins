pipeline{
	stages{
		stage('Maven build'){
			steps{
				ansiblePlaybook(inventory: 'inventory.ini', playbook: 'build_playbook.yaml')
			}
		}
	}
}
