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
three.example.com.

```

- An Ansible role has a defined directory structure with seven main standard directories. You must include at least one of these directories in each role. You can omit any directories the role does not use. For example:

# playbooks
```site.yml
webservers.yml
fooservers.yml
roles/
    common/
        tasks/
        handlers/
        library/
        files/
        templates/
        vars/
        defaults/
        meta/
    webservers/
        tasks/
        defaults/
        meta/
 ```
#### Become directives
You can set the directives that control become at the play or task level. You can override these by setting connection variables, which often differ from one host to another. These variables and directives are independent. For example, setting become_user does not set become.

become
set to yes to activate privilege escalation.

become_user
set to user with desired privileges — the user you become, NOT the user you login as. Does NOT imply become: yes, to allow it to be set at host level. Default value is root.

become_method
(at play or task level) overrides the default method set in ansible.cfg, set to use any of the Become Plugins.

become_flags
(at play or task level) permit the use of specific flags for the tasks or role. One common use is to change the user to nobody when the shell is set to nologin. Added in Ansible 2.2.

For example, to manage a system service (which requires root privileges) when connected as a non-root user, you can use the default value of become_user (root):

- To run ansible playbook command is `ansible-playbook <playbook.yml>`
