# ansible-playbooks

# how to use

```
sudo apt-get install sshpass
cd /path/to/ansible-playbooks/yumaatt
touch private_vars/admin{, -development, -development-vagrant_ubuntu14}.yml
vim private_vars/admin-development.yml
ansible-playbook site.yml -i hosts -l admin-development-vagrant_ubuntu14 -k -C
ansible-playbook site.yml -i hosts -l admin-development-vagrant_ubuntu14 -k

cd /path/to/ansible-playbooks/yumaatt
touch private_vars/test{, -development, -development-test_ubuntu14}.yml
vim private_vars/test-development.yml
touch private_vars/admin{, -development, -development-mac}.yml
ansible-playbook site.yml -i hosts -l test-development-test_ubuntu14 -C
ansible-playbook site.yml -i hosts -l test-development-test_ubuntu14
```

todo
```
vim ~/.gitconfig.local
emacs --debug-init
aws configure
```
