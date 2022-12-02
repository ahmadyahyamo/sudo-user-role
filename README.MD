# Ansible role to create a user with  sudo rights

1. update the inventory file with the list of target servers and locate your private key to connect to the target servers
2. by default this role will create a user named "bigdata_user" and will put it's public key in the authorized keys file on the target servers

# Run ansible playbook
    ansible-playbook -i inventory main.yaml

# Run with different variables other than the default
    ansible-playbook -i inventory main.yaml -e '{"pub_key_file":"/home/ahmad/IdeaProjects/ansible/roles/sudo-user/files/bigdata_user.pub","username":"testing"}'