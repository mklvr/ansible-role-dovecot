ansible-role-dovecot
=========

The simplest dovecot config to get things off the ground. We use local auth for or limited number of users.

Requirements
------------

Nothing special.

Role Variables
--------------

In `defaults/main.yml`, the variable `dovecot_ssl_key` is defined as  `<{{ openssl_private_key['filename'] }}`. The latter will only be defined if you run the `ansible-role-acme-cert` role prior to this one.

Dependencies
------------

`mklvr/ansible-role-acme-cert` is a dependency unless you want to redefine some variables.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible-role-acme-cert # See above.
         - ansible-role-dovecot

License
-------

MIT

Author Information
------------------

Mike Oliver (mike@mklvr.io)
