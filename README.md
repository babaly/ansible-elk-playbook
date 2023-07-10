# Ansible ELK Playbook
 
This playbook is for setting up version 5.x of the ELK Stack on a remote server. 

## Notes and requirements

 - The playbook was built and tested on Ubuntu 22.04 VMs, for ELK versions 5.x 
 - You will need Ansible installed and running
 - Playbook is currently configured to set up the ELK stack together with Metricbeat for server perf monitoring.
 
 ## Instructions
 
 1. Edit your Ansible hosts file ('/etc/ansible/hosts') and add an 'elkservers' entry for the server you wish to install ELK on. You can of course name the host any way you want, this is just an example. 
 2. Or use your ouwn inventory file named hosts in the route directory	
 3. create a ssh key and copy it to the remote host 
 4. Verify connectivity to the ELK server with the ping module.
 5. In the terminal on the machine hosting Ansible, clone this repo.
 6. Cd into the directory, and run:
 `ansible-playbook main.yml -i hosts -u remote_user(ubuntu in the main.yml) -K`
 
 
 The plays in the playbook will run on the target server, installing ELK and the specified beats shippers. 

