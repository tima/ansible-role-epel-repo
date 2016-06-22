# Ansible Role: epel-repo

[![Build Status](https://travis-ci.org/tima/ansible-role-epel-repo.svg?branch=master)](https://travis-ci.org/tima/ansible-role-epel-repo)

Sets up EPEL release and/or testing repository on RedHat/CentOS OS family servers. 

Uses the epel-release and epel-testing yum packages.

This role handles skipping its tasks for other OS types.

## Requirements

None

## Role Variables

Available variables are listed below with default values (see `defaults/main.yml`):

    epel_repo_release: True

This boolean variable enables the setup of the EPEL release (stable) repository.

    epel_repo_release_state: present

The yum state of the epel-release package on the host.

    epel_repo_testing: False

This boolean variable enables the setup of the EPEL testing repository.

    epel_repo_testing_state: present

The yum state of the epel-testing package on the host.


## Dependencies

None

## Example Playbook

The most basic usage of this role in a play is as follows:

    - hosts: servers
      roles:
         - role: 'tima.epel-repo'

To setup the EPEL release and testing channels:

    - hosts: servers
      roles:
         - role: 'tima.epel-repo'
           epel_repo_testing: True

## Contributions and Feedback

Any contributions are welcome. For any bugs or feature requests,
please open an issue through Github.

## License

Apache

## Author

Created by [Timothy Appnel](https://github.com/tima).
