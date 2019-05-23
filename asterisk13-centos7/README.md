Role Name
=========
asterisk13-centos7

Installs Asterisk13 & FreePBX on a base Centos7 host
Installs Asterisk, Dahdi, Libpri and FreePBX on a base Centos7 box.


Requirements
------------

ansible 2.7.10
May or may not be backward-compatible with older versions of Asterisk
All testing was done on Google Cloud VM Instances, using the standard Centos7 x86_64 built on 20190326


Role Variables
--------------

All role variables can be found in the defaults/main.yml

Dependencies
------------
In /tasks/main.yml comment out the asterisk_dahdi_install.yml task if target is a virtual host or no telephony hardware is being installed.
 include_tasks: asterisk_dahdi_install.yml

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: asterisk13-centos7, x: 42 }
         
Execute
--------
    ansible-playbook playbook.yml --private-key=~/.ssh/keyname -i hosts -u username -b

License
-------

BSD

Author Information
------------------

https://github.com/Redfone/
