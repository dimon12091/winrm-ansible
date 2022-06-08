# Ansible Server Setup
These scripts and configs help setup the ansible server to communicate to the windows host via WinRM.
```commandline
export OPENSSSL_CONF=openssl.conf
./generate_client_cert.sh
```
Test ping to remote server.
```commandline
ansible all -i <your inventory file> -m win_ping
```
Main step. Install dependencies and copy project to remote server.
```commandline
ansible-playbook -i <your inventory file> deploy.yml
```
After main step, you can run the tool manually pssetools.
```commandline
ansible-playbook -i <your inventory file> run_on_demand.yml
```
After main step, you can run scheduler task( pssetools ) in windows.
```commandline
ansible-playbook -i <your inventory file> setup_scheduler.yml
```
