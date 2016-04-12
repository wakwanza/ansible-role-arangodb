Ansible Role: arangoDB
=========

[![Build Status](https://travis-ci.org/wakwanza/ansible-role-arangodb.svg?branch=master)](https://travis-ci.org/wakwanza/ansible-role-arangodb) [![DUB](https://img.shields.io/dub/l/vibe-d.svg)]()

An Ansible Role that installs arangoDB on RedHat/CentOS,Debian/Ubuntu or OpenSUSE.


Requirements
------------

Works on Linux versions based on Enterprise Linux (CentOS/RedHat >=6), Debian (jessie & wheezy), Ubuntu (precise and later) and openSUSE.
On EL based distributions SELINUX needs to be set to permissive for some of the tasks to work.

Role Variables
--------------

<table>
    <tr>
        <td>`storage_directory_base`</td> <td>Directory root to store data and metadata.Defaults to /var/lib/arangodb</td>
    </tr>
        <tr>
        <td>`ssl_cert_location`</td> <td>Directory for the certificates to use for TLS connection , inter-cluster as well as client-server connections.Defaults to /etc/ssl/certs.</td>
    </tr>

</table>

For secure installation the TLS connections between nodes, to clients are enabled and the http-admin page is disabled.
Further tuning possible by modifying values in 'templates/arangod.j2'.

Example Playbook
----------------

Install the role using galaxy : ansible-galaxy install wakwanza.arangodb

    - hosts: nosqldb
      roles:
         - { role: wakwanza.arangodb }

License
-------

MIT

Author Information
------------------

@wakwanza Abdulrahim Umar.
