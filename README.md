authy-ssh
=========

[![Build Status](https://img.shields.io/travis/marvinpinto/ansible-role-authy-ssh/master.svg?style=flat-square)](https://travis-ci.org/marvinpinto/ansible-role-authy-ssh)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-authy--ssh-blue.svg?style=flat-square)](https://galaxy.ansible.com/marvinpinto/authy-ssh)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.txt)

Ansible role to install and configure [Authy 2FA for
SSH](https://github.com/authy/authy-ssh) logins.

Requirements
------------

This role has been tested on Ubuntu 14.04 and will likely only work on an
Ubuntu-like system. You will need an [Authy API
key](https://www.authy.com/signup) as well as a already-configured 2FA user.

Role Variables
--------------

```yaml
---
- tbd: "work in progress"
```

Examples
--------

Install this module from Ansible Galaxy into the './roles' directory:
```bash
ansible-galaxy install marvinpinto.authy-ssh -p ./roles
```

Use it in a playbook as follows:
```yaml
- hosts: '127.0.0.1'
  roles:
    - role: 'marvinpinto.authy-ssh'
      sudo: true
```
