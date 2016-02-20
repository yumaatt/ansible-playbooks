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
