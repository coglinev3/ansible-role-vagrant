# Ansible Role: vagrant

[![Build Status](https://travis-ci.com/coglinev3/ansible-role-vagrant.svg?branch=master)](https://travis-ci.com/coglinev3/ansible-role-vagrant) ![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/coglinev3/ansible-role-vagrant) [![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://raw.githubusercontent.com/coglinev3/ansible-role-vagrant/master/LICENSE)

This Ansible role installs HashiCorp [Vagrant](https://www.vagrantup.com/intro "Introduction to Vagrant") on these supported Linux distributions:

* Debian 8 (Jessie),
* Debian 9 (Stretch),
* Debian 10 (Buster),
* Enterprise Linux 7, 
* Enterprise Linux 8, 
* Fedora 32,
* Linux Mint 20 Ulyana,
* Ubuntu 16.04 LTS (Xenial Xerus),
* Ubuntu 18.04 LTS (Bionic Beaver),
* Ubuntu 20.04 LTS (Focal Fossa),

This Role was tested with [Travis CI](https://travis-ci.com/coglinev3/ansible-role-vagrant "Travis CI") using [Docker](https://www.docker.com/ "Docker") and  with a [multi virtual machine Vagrant environment](https://ansible-development.readthedocs.io "Environment for developing and testing Ansible roles").

## Requirements

None


## Role Variables

Available variables are listed below, along with default values:

```yml
# variables for Hashicorps's signing key
hashicorp_public_key: "https://apt.releases.hashicorp.com/gpg"
hashicorp_public_key_state: present

# Vagrant packages to be installed
vagrant_packages:
  - vagrant
#  - vagrant-hostmanager
#  - vagrant-sshfs
#  - vagrant-libvirt
#  - vagrant-mutate
#  - nfs-kernel-server

vagrant_packages_state: present

# define dependencies for vagrant
vagrant_dependencies:
  - apt-transport-https
```

## Dependencies

None


## Example Playbook

```yml
---
# file: tests/test.yml

- hosts: localhost
  roles:
    - { role: coglinev3.vagrant }
```

## Version

Release: 1.0.2


## License

BSD


## Author Information

Copyright &copy; 2020 Cogline.v3.
