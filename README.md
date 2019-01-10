
#### Description

- Ansible playbooks to modify sudoers file:
- add_to_sudoers.yml - add a new user to sudoers.
- remove_from_sudoers.yml - remove user from sudoers.


#### prerequisites

- Ansible Installed >v2.4.
- create inventory file with your target server.
- populate ssh key from your ansible server to all target servers.

#### execute via cli

- add a new user: ansible-playbook -i <your inventory file> add_to_sudoers.yml -e "SUDO_USER='you_new_user"
- remove a user: ansible-playbook -i <your inventory file> remove_from_sudoers.yml --extra-var "SUDO_USER='user_to_remove'"
