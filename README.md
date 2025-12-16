# Ansible Role: vagrant

[![Build](https://github.com/coglinev3/ansible-role-vagrant/actions/workflows/build.yml/badge.svg)](https://github.com/coglinev3/ansible-role-vagrant/actions/workflows/build.yml) ![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/coglinev3/ansible-role-vagrant) [![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://raw.githubusercontent.com/coglinev3/ansible-role-vagrant/master/LICENSE)

This Ansible role installs HashiCorp [Vagrant](https://www.vagrantup.com/intro "Introduction to Vagrant") on these supported Linux distributions:

* AmazonLinux 2023,
* Debian 11 (Bullseye),
* Debian 12 (Bookworm),
* Debian 13 (Trixie),
* Enterprise Linux 9, 
* Enterprise Linux 10, 
* Fedora 40,
* Fedora 41,
* Fedora 42,
* Ubuntu 22.04 LTS (Jammy Jellyfish),
* Ubuntu 24.04 LTS (Noble Numbat).

The role was tested with [Ansible Molecule](https://molecule.readthedocs.io/en/latest/ "Ansible Molecule") and [Docker](https://www.docker.com/ "Docker").

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

vagrant_packages_state: present

# define dependencies for vagrant
vagrant_dependencies:
  - apt-transport-https
  - gpg
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

Release: 1.2.0


## License

BSD


## Author Information

Copyright &copy; 2023 Cogline.v3.
