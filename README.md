# vagrant-practice
Messing about with vagrant and virtualbox, as recommended by the book: Ansible for
DevOps by Jeff Geerling.

## Prerequisites
Install `vagrant` and `virtualbox` as prerequisites.

## Usage
Run the following commands in a directory of your choice:

Get a CentOS7 image by geerlingguy:
```
vagrant box add geerlingguy/centos7
```

Create a default virtual server configuration:
```
vagrant init geerlingguy/centos7
```

Boot the server:
```
vagrant up
```

Halt the server:
```
vagrant halt
```

Delete the machine:
```
vagrant destroy
```

Connect to the server via SSH:
```
vagrant ssh
```

Get more SSH details:
```
vagrant ssh-config
```
