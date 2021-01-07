# overcloud-gather

## Description

Simple Ansible playbook to gather overcloud nodes' sosreports to a local directory and eventually upload them to a customer case at Red Hat.

## Usage

1. Clone repo
~~~
(undercloud) [stack@undercloud-0 ~]$ git clone https://github.com/mauroseb/overcloud-gather.git
~~~

2. Set the variables as needed at overcloud-gather/overcloud.gather.yml
  - Subset of roles or nodes to gather from
  - Case number
  - Upload if required
  - Delete local directory if required

3. Run playbook passing tripleo-ansible-inventory
~~~
(undercloud) [stack@undercloud-0 ~]$ ansible-playbook -i /usr/bin/tripleo-ansible-inventory overcloud-gather/overcloud-gather.yml
~~~

