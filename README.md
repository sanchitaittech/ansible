# ansible
Ansible Project
## Steps to start VMs
```
vagrant up --provider=hyperv
```
## Create initial user "centos"

#### Create encryted password/text using:
```
mkpasswd --method=sha-512

```

#### Create variable in hosts called user_hash with output text of above command and use it user module
user_hash=<output from above command>

```
ansible-playbook -k user.yml
```


