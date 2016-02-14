# ansible-playbooks

# how to use

```
sudo apt-get install sshpass
cd /path/to/ansible-playbooks/yumaatt
ansible-playbook site.yml -i development -l vagrant_ubuntu14 -k -C
ansible-playbook site.yml -i development -l vagrant_ubuntu14 -k

cd /path/to/ansible-playbooks/yumaatt
ansible-playbook site.yml -i development -l test_ubuntu14 -C
ansible-playbook site.yml -i development -l test_ubuntu14
```
