# nginx-php-fpm installation on CentOS 6/7 or Ubuntu 18.04/Debian9

You need minimum 1GB RAM for succesfully run playbook.

Software version.

Ansible 2.7.5

Centos 6/7

Postfix: 3.3.0

Dovecot: 2.2.33.2

mysql Ver 14.14 Distrib 5.7.25

SpamAssassin version 3.4.2


run command: 

yum install git ansible mc python2-PyMySQL -y

or

apt update && apt install git ansible mc -y
mkdir /etc/ansible/roles

for Debian like distros

git clone https://github.com/Nurlan199206/ansible-lemp

and

ansible-playbook --connection=local -s /etc/ansible/roles/mailserver/nginx.yml



for successfully run playbook, dont forget add in /etc/ansible/ansible.cfg after [defaults]

invalid_task_attribute_failed=False
