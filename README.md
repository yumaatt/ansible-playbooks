# ansible-playbooks

# how to use

```
git clone https://github.com/yumaatt/ansible-playbooks.git /path/to/ansible-playbooks

# vagrant
sudo apt-get install sshpass
cd /path/to/ansible-playbooks/yumaatt
touch private_vars/admin{,-development,-development-vagrant_ubuntu14}.yml
//vim private_vars/admin.yml
vim private_vars/admin-development.yml
//vim private_vars/admin-development-vagrant_ubuntu14.yml
ansible-playbook site.yml -i hosts -l admin-development-vagrant_ubuntu14 -t create_user -k -C
ansible-playbook site.yml -i hosts -l admin-development-vagrant_ubuntu14 -t create_user -k
ansible-playbook site.yml -i hosts -l admin-development-vagrant_ubuntu14 -k -C
ansible-playbook site.yml -i hosts -l admin-development-vagrant_ubuntu14 -k

# mac
cd /path/to/ansible-playbooks/yumaatt
touch private_vars/admin{,-development,-development-mac}.yml
//vim private_vars/admin.yml
//vim private_vars/admin-development.yml
//vim private_vars/admin-development-mac.yml
ansible-playbook site.yml -i hosts -l admin-development-mac -K -C
ansible-playbook site.yml -i hosts -l admin-development-mac -K

# test ubuntu14
cd /path/to/ansible-playbooks/yumaatt
touch private_vars/test{,-development,-development-test_ubuntu14}.yml
//vim private_vars/test.yml
vim private_vars/test-development.yml
//vim private_vars/test-development-test_ubuntu14.yml
ansible-playbook site.yml -i hosts -l test-development-test_ubuntu14 -t create_user -C
ansible-playbook site.yml -i hosts -l test-development-test_ubuntu14 -t create_user
ansible-playbook site.yml -i hosts -l test-development-test_ubuntu14 -C
ansible-playbook site.yml -i hosts -l test-development-test_ubuntu14

# phoply dev1
cd /path/to/ansible-playbooks/yumaatt
touch private_vars/phoply{,-development,-development-phoply_dev1}.yml
//vim private_vars/phoply.yml
vim private_vars/phoply-development.yml
//vim private_vars/phoply-development-phoply_dev1.yml
ansible-playbook site.yml -i hosts -l phoply-development-phoply_dev1 -t create_user -C
ansible-playbook site.yml -i hosts -l phoply-development-phoply_dev1 -t create_user
ansible-playbook site.yml -i hosts -l phoply-development-phoply_dev1 -C
ansible-playbook site.yml -i hosts -l phoply-development-phoply_dev1
```

when you create new app setting
```
# new app
cd /path/to/ansible-playbooks/yumaatt
NEW_APP=xxx
NEW_APP_CONTAINER=yyy
touch private_vars/${NEW_APP}{,-development,-development-${NEW_APP_CONTAINER}}.yml
//vim private_vars/${NEW_APP}.yml
vim private_vars/${NEW_APP}-development.yml
//vim private_vars/${NEW_APP}-development-${NEW_APP_CONTAINER}.yml
touch group_vars/${NEW_APP}{,-development,-development-${NEW_APP_CONTAINER}}.yml
//vim group_vars/${NEW_APP}.yml
vim group_vars/${NEW_APP}-development.yml
vim group_vars/${NEW_APP}-development-${NEW_APP_CONTAINER}.yml
vim site.yml
ansible-playbook site.yml -i hosts -l ${NEW_APP}-development-${NEW_APP_CONTAINER} -C
ansible-playbook site.yml -i hosts -l ${NEW_APP}-development-${NEW_APP_CONTAINER}
```

todo(centos6)
```
wget http://ftp.jaist.ac.jp/pub/GNU/emacs/emacs-24.4.tar.gz
tar xvf emacs-24.4.tar.gz
cd emacs-24.4
./configure
sudo make
sudo make install
```

todo
```
open vim and exec :NeoBundleInstall
emacs --debug-init
vim ~/.gitconfig.local
aws configure
```
