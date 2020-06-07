# tobias_richter.python

[![Build Status](https://travis-ci.org/tobias-richter/ansible-python.svg?branch=master)](https://travis-ci.org/tobias-richter/ansible-python)

This role setups python3 and installed setuptools and python with the
configured versions.

The role also setups a custom `global_index_url` in `/etc/pip.conf` if
configured.

## Requirements

This role requires Ansible 2.7 or higher.

## Role Variables

See [defaults/main.yml](defaults/main.yaml) for the documented role
variables.

## Example Playbook

This playbook setups python with a custom Sonatype nexus based pypi
cache.

    - hosts: python
	  roles:
	    - role: tobias_richter.python
	      python_global_index_url: https://nexus.main.corp/repository/pypi/simple