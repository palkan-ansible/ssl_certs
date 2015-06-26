SSL certs management
=========

Copy SSL certs and keys to remote host by simply providing one variable.

Installation
--------------

`ansible-galaxy install palkan.ssl_certs`

Role Variables
--------------
| Name                        | Description    | Example |
|-----------------------------|---------------|-----------------|
| ssl_certs          | A list of certs | - { src: 'path/to/my_cert.crt', name: 'my_app', dir: '/etc/ssl/certs'}|
| ssl_keys          | A list of private keys | - { src: 'path/to/my_key.key', name: 'my_app', dir: '/etc/ssl/private'}|

Example Playbook
----------------
    - hosts: servers
      roles:
         - { role: palkan.ssl_certs }
