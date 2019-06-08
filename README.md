## What is ansible-dhparam? [![Build Status](https://travis-ci.com/Duckle29/ansible-dhparam.svg?branch=master)](https://travis-ci.com/Duckle29/ansible-dhparam)

It is an [Ansible](http://www.ansible.com/home) role to:

- Generate a dh-parameter file on your local machine
- Move it to a target server

## Role variables

``` yaml
dhparams_key_size: 4096
dhparams_remote_directory: /etc/ssl/ansible
dhparams_filename: dhparams.pem
dhparams_owner: root
dhparams_group: root
dhparams_mode: u=rw,g=r,o=r
dhparams_directory_mode: u=rw,g=r,o=r
```

## Example usage

``` yaml
---
- name: Generate dhparams for remote server
  hosts: all

  vars:
    dhparams_key_size: 2048

  roles:
    - role: duckle29.dhparam

```

## Installation

`$ ansible-galaxy install duckle29.dhparam`

## Ansible Galaxy

You can find it on the official
[Ansible Galaxy](https://galaxy.ansible.com/duckle29/dhparam/) if you want to rate it.

## License

MIT
