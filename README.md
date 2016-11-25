## Standalone Tomcat Deployment to ubuntu Os

- Requires Ansible 1.2 or newer
- Expects Ubuntu hosts
- Install Openjdk 1.8
- Install Tomcat7 or 8

These playbooks deploy a very basic implementation of Tomcat Application Server,
version 7 or 8. To use them, first edit the "hosts" inventory file to contain the
hostnames of the machines on which you want Tomcat deployed, and edit the
group_vars/tomcat-servers file to set any Tomcat configuration parameters you need.

Then run the playbook, like this:

For Tomcat7 :

	ansible-playbook -i hosts site.yml --extra-vars "version=7"

For Tomcat8 :

	ansible-playbook -i hosts site.yml --extra-vars "version=8"
	
When the playbook run completes, you should be able to see the Tomcat
Application Server running on the ports you chose, on the target machines.

This is a very simple playbook and could serve as a starting point for more
complex Tomcat-based projects.

### Ideas for Improvement

Here are some ideas for ways that these playbooks could be extended:

- Write a playbook to deploy an actual application into the server.
- Deploy Tomcat clustered with a load balancer in front.

We would love to see contributions and improvements, so please fork this
repository on GitHub and send us your changes via pull requests.

@Inforedaster
