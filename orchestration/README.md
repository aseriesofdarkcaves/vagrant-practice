# orchestration
Sets up 3 VM hosts.
Added a `hosts.ini` file in the repo instead of editing `/etc/hosts`.
Not sure how to get DNS working yet, so the IPs are being used in the `hosts.ini` file.
Changed the hostgroup name from multi to all.

## Usage
```
# set up the VMs using the provided vagrantfile
vagrant up

# a few ad-hoc commands to play about with
ansible all -a "hostname" -i hosts.ini
ansible all -a "df -h" -i hosts.ini
ansible all -a "free -m" -i hosts.ini
ansible all -a "date" - i hosts.ini
ansible all -m setup -i hosts.ini
ansible all -b -m yum -a "name=ntp state=present" -i hosts.ini
```