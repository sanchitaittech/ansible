# ansible
Ansible Project
## Steps to start VMs
```
vagrant up --provider=hyperv
```
## Create initial user "centos"

#### Create encryted password/text/using:
```
mkpasswd --method=sha-512

```

#### Create variable in call user_hash with output text of above command and use it user module


```
ansible all -u root -m user -a "name=centos shell=/bin/bash groups=wheel password={{ user_hash }} update_password=always"

```
