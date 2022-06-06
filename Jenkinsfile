pipeline{
	agent { node { label 'linuxagent' } }
        
	tools{
            maven 'maven-3.8.5'
            git 'Default'
	}

	stages{
		stage('Maven build'){
			steps{
				ansiColor('xterm') {
					ansiblePlaybook(inventory: 'inventory.ini', playbook: 'build_playbook.yaml',colorized: true)
				}
			}
		}
		stage('WAR File copy to Tomcat server'){
			steps{
				ansiColor('xterm') {
					ansiblePlaybook(inventory: 'inventory.ini', playbook: 'copy_war_tomcat_playbook.yaml',colorized: true)
				}
			}
		}
	}
}
