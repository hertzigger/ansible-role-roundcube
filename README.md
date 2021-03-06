marklee77.roundcube
===================

[![Build Status](https://travis-ci.org/marklee77/ansible-role-roundcube.svg?branch=master)](https://travis-ci.org/marklee77/ansible-role-roundcube)

roundcube webmail

Requirements
------------

MySQL or MariaDB

Role Variables
--------------

- roundcube_run_dir: "{{ lookup('env', 'PWD') }}"
- roundcube_root_mysql_password: "{{ lookup('password', roundcube_run_dir + '/private/credentials/root-mysql-password') }}"
- roundcube_roundcube_mysql_password: "{{ lookup('password', roundcube_run_dir + '/private/credentials/roundcube-mysql-password') }}"
- roundcube_des_key: "{{ lookup('password', roundcube_run_dir + '/private/credentials/roundcube-des-key length=24') }}"

- roundcube_hostname: localhost
- roundcube_http_port: 80
- roundcube_https_port: 443
- roundcube_enable_ssl: true
- roundcube_require_ssl: true

- roundcube_ssl_cert_file: ""
- roundcube_ssl_key_file: ""

- roundcube_imap_host: localhost

Example Playbook
-------------------------

    - hosts: all
      sudo: True
      roles:
        - marklee77.roundcube

License
-------

GPLv2

Author Information
------------------

Mark Stillwell

http://stillwell.me

