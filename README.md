# K3s-Pi4-Cluster-Rollout

## requirements
- pi4 with active Raspbian-Lite-64bit-Image and ssh-access
- ansible on your local-machine
- add IPs of each raspberry to /etc/ansible/hosts on your local-machine

test if all hosts are reachable via `ansible -m ping master,workers`

## run
```bash
ansible-playbook ./playbooks/k3s/install.yml 
```