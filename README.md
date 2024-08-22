# K3s-RaspberryPi-Cluster-Rollout

Rollout K3s on multiple Raspberry-Pis via Ansible.

## Requirements
- Raspberry-Pi-4 with Raspbian-Lite-64bit-Image and SSH-access
- Ansible >= [core 2.16.3] on your local-machine 
- Add IPs of each raspberry to /etc/ansible/hosts on your local-machine

Check if ansible is installed

```bash
ansible --version
# ansible [core 2.16.3]
# ...
```

Edit `/etc/ansible/hosts` and add all your Raspberry-Pi's:

```bash
[master]
# <raspi-ip-1>

[workers]
# <raspi-ip-2>
# <raspi-ip-3>
# <raspi-ip-4>
# <raspi-ip-5>
# ...
```

## Test 

Test if all hosts are reachable via:

```bash
ansible -m ping master,workers
```


## Run 

Execute Rollout if Requirements are fullfilled via:

```bash
ansible-playbook ./playbooks/k3s/install.yml 
```