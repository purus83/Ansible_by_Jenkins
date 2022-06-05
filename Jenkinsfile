pipeline{
	agent { node { label 'linuxagent' } }
        
	tools{
            maven 'maven-3.8.5'
            git 'Default'
	}
	
	stages{
		stage('Maven build'){
			steps{
				ansiblePlaybook(inventory: 'inventory.ini', playbook: 'build_playbook.yaml')
			}
		}
	}
}
