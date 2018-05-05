Let's encrypt
=============

This is an ansible role to install and use ansible. It can either be used in
a playbook to certify several domains or in a task to certify a specific
domain.

Role Variables
--------------

### letsencrypt\_domains

default value: []

Override this variable to choose domains to certify.

### letsencrypt\_webroot

default value: /var/lib/letsencrypt

This variable defines the webroot used by letsencrypt to resolve the challenges.

### letsencrypt\_email

default value: null

**required**

You must override this setting to be alerted when a certificate will expire

### letsencrypt\_domains\_directory

default value: /etc/letsencrypt/live

This is the directory where certificates for your domains are stored.

### letsencrypt\_tos\_agreed

default value: false

Read https://letsencrypt.org/repository/ and set this to true


Example Playbook
----------------

    - hosts: servers
      roles:
        - role: Shir0kamii.letsencrypt
	  vars:
	    - letsencrypt_domains:
		  - example.com

License
-------

MIT

Contribute
----------

For now this role only works for debian but feel free to contribute to add support for another support. This project is maintained.
