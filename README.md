# Ansible configuration to do Performance testing with JMeter and Jenkins

## 1- Set hosts in ~/.ssh/config file
Host ubuntu-master-1
    HostName xxx.xxx.xxx.xxx
    User ubuntu
    IdentityFile /path/to/pem/file
 
Host ubuntu-slave-1
    HostName xxx.xxx.xxx.xxx
    User ubuntu
    IdentityFile /path/to/pem/file

## 2- Config the hosts file in Ansible
[master]

ubuntu-master-1

[slaves]

ubuntu-slave-1

## 3- Install the common playbook in all hosts
$ ansible-playbook 01-common-playbook.yaml -b

## 4- Install the slave playbook
$ ansible-playbook 02-slave-playbook.yaml -b

## 5- Install the master-instance playbook to install Jenkins
$ ansible-playbook master-instance.yaml -b

## 6- Create a folder that contains the .jmx file

## 7- Use the copy_jmx.yaml file to copy the folder with jmx file and install the required plugins for the test
$ ansible-playbook copy_jmx.yaml -b


