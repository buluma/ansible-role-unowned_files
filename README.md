# Ansible role [unowned_files](https://galaxy.ansible.com/ui/standalone/roles/buluma/unowned_files/documentation)

Install and configure unowned_files on your system.

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-unowned_files/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-unowned_files/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-unowned_files.svg)](https://github.com/buluma/ansible-role-unowned_files/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-unowned_files.svg)](https://github.com/buluma/ansible-role-unowned_files/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-unowned_files.svg)](https://github.com/buluma/ansible-role-unowned_files/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/unowned_files)](https://galaxy.ansible.com/ui/standalone/roles/buluma/unowned_files/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-unowned_files/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  roles:
    - role: buluma.unowned_files
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-unowned_files/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: true
  gather_facts: false

  roles:
    - role: buluma.bootstrap
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-unowned_files/blob/master/defaults/main.yml):

```yaml
---
# defaults file for unowned_files

# What to do with files or directories that have no owner. `yes` will detele
# files that have either no owner or group. `no` will change the ownership of
# files to the user and group set with `unowned_files_default_owner` and
# `unowned_files_default_group`.
unowned_files_delete: false

# If files have no owner, but do have a group, change the owner to this
# variable.
unowned_files_default_owner: nodody

# If files have no group, but do have an owner, change the group to this
# variable.
unowned_files_default_group: nodody

# A list of paths to search
unowned_files_directories:
  - /
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-unowned_files/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-unowned_files/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Alpine](https://hub.docker.com/r/buluma/alpine)|all|
|[Amazon](https://hub.docker.com/r/buluma/amazonlinux)|Candidate|
|[EL](https://hub.docker.com/r/buluma/enterpriselinux)|8|
|[Debian](https://hub.docker.com/r/buluma/debian)|all|
|[Fedora](https://hub.docker.com/r/buluma/fedora)|all|
|[opensuse](https://hub.docker.com/r/buluma/opensuse)|all|
|[Ubuntu](https://hub.docker.com/r/buluma/ubuntu)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-unowned_files/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-unowned_files/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-unowned_files/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)
