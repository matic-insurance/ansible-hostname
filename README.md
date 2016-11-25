Role Name
=========

Set hostname with /etc/hosts on Debian-based systems.

Debian-based distros encourage you to set non-FQDN hostname ([more](More: http://serverfault.com/questions/331936/setting-the-hostname-fqdn-or-short-name)), so this role uses first chunk of FQDN-hostname as hostname.

Requirements
------------

This role works only on Debian-based systems. Tested on Ubuntu 14.04

Role Variables
--------------

You need to provide:

* `fqdn_hostname`: FQDN-hostname

Also you can override:

* `short_hostname`: hostname used in `/etc/hostname`. *Default: first chunk of `fqdn_hostname`*

Dependencies
------------

No dependencies

Example Playbook
----------------

    - role: matic-insurance.hostname
      fqdn_hostname: '{{ inventory_hostname }}'
      tags: ['hostname']

License
-------

MIT

Author Information
------------------

Matic is a communication platform that connects lenders and borrowers originating a new home loan. A borrower now knows where they are in the loan process and what they need to do to complete the loan.
