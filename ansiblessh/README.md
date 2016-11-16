# Ansible which deploys SSH Pub keys onto remote host(s) from a file or parsed from Json

## Pre-Requirements
- Vagrant installed on host machine from trying the ansible
- Clone this folder/repo locally and bring up the vagrant machine by issuing:
````ruby
vagrant up
````

## Ansible SSH deploy - From Json file

Run ansible for updating the recently launched host with the SSH keys from remote github account
````
export ANSIBLE_HOST_KEY_CHECKING=False
ansible-playbook -i hosts ansiblessh.yml --private-key=/home/username/.vagrant/insecure_private_key --tags "fromjson"
````

## Ansible SSH deploy - From pub key file

Run ansible for updating the recently launched host with the SSH keys from remote github account
````
export ANSIBLE_HOST_KEY_CHECKING=False
ansible-playbook -i hosts ansiblessh.yml --private-key=/home/username/.vagrant/insecure_private_key --tags "frompubkey"
````

## Troubleshooting

- You may want to change the --private-key and url used within the ansible to your choice
