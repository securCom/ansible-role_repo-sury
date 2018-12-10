[![Build Status](https://www.travis-ci.org/securCom/ansible-role_repo-sury.svg?branch=master)](https://www.travis-ci.org/securCom/ansible-role_repo-sury)
[![GitHub release](https://img.shields.io/github/release/securCom/ansible-role_repo-sury.svg)](https://github.com/securCom/ansible-role_repo-sury)

# Repo: Sury

Manage  Sury repository collections

# Requirements

For supported systems  see https://packages.sury.org. If your system is not supported,
the role tasks will be skipped.

For supported system by this role, see the `vars/os-<system>` files.

For supported repositories for given system see variable `sury_repo_supported` in `vars/os-<system>`.

Feel free to add any new linux distribution and version if missing.

# Role Variables

- `sury_repo_state`: the sury package presence  state
- `sury_repo_name`(required): name of the repository to install, one from the list `sury_repo_supported`

# Dependencies

There no external dependencies.

# Example Playbook

To install role, add following line to **ansible-galaxy** requirements file
```
- src: https://github.com/securCom/ansible-role_repo-sury
  version: master
  name: securcom.repo_sury
```

```
- hosts: servers
  roles:
     - { role: securcom.repo_sury, sury_repo_name: 'php' }
```

# License

BSD

# Author Information


- Peter Hudec (@hudecof)