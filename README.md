# About Repository

- It is basically automated ansible playbook and roles  to create kubernetes multinode cluster.
- Ansible roles will create master node , worker node and deploy pods over the worker node.

### Setup

- To install ansible `$ sudo yum install ansible` for RHEL8 and Centos.
- The inventory file can be in one of many formats, depending on the inventory plugins you have. The most common formats are INI and YAML. A basic INI /etc/ansible/hosts might look like this:

```mail.example.com

[webservers]
foo.example.com
bar.example.com

[dbservers]
one.example.com
two.example.com
three.example.com```
