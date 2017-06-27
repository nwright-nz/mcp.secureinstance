Role Name
=========

This role will help secure a linux server created with just password authentication. This will disable password auth, disable the root remote login, and inject a certificate to be used for the provided user. This is primarily being used for servers in 
the Dimension Data Managed cloud platform.

Requirements
------------

Public/Private keys created    

Role Variables
--------------

```yaml
user: <<the username you want to use to login>>
path_to_public_key: <<path the created SSH public key. You can create a new one with the command: ssh-keygen -t rsa
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: mcp.secureinstance, user: cloud-user, path_to_public_key: '~/.ssh/my_pub_key.pub }
```
License
-------

BSD

Author Information
------------------

Nigel Wright
nigel.wright@dimensiondata.com
@nigelwright_nz

