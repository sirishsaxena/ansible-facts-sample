# ansible-facts-sample

This project is an example of how to use ansible facts to make decisions in playbooks. The playbook in playbook.yml installs apache on both Debian- and CentOS-based hosts, using ansible facts to determine which packages to install.

## Additional Resources

[Ansible facts](http://docs.ansible.com/ansible/latest/playbooks_variables.html#information-discovered-from-systems-facts) documentation.

[Ansible when statement](http://docs.ansible.com/ansible/latest/playbooks_conditionals.html#the-when-statement) documentation.