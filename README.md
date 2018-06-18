# wilmardo.tautulli

[![Build Status](https://travis-ci.org/wilmardo/ansible-role-domoticz.svg?branch=master)](https://travis-ci.org/wilmardo/ansible-role-tautulli)
[![Galaxy](https://img.shields.io/badge/galaxy-wilmardo.tautulli-blue.svg)](https://galaxy.ansible.com/wilmardo/tautulli/)

Role to install tautulli

## Requirements

None.

## Role Variables

### Default usage

As default tautulli is installed and running.
If you want to adapt this to your needs look at the [Advanced usage](#advanced-usage) section.

### Advanced usage

For more advanced usage the following variables are available:
```yaml
# Version of Tautulli to install, gets passed to the Ansible git module
tautulli_version: v2.0.28
# User to run tautulli as
tautulli_user: tautulli
# Group to run tautulli as
tautulli_group: tautulli
# Tautulli install location
tautulli_install_location: /opt/Tautulli/
# Tautulli configuration location (recommended is to put it somewhere in /etc)
tautulli_config_location: /etc/tautulli-config.ini
# Tautulli data location (recommended is to NOT put it in your Tautulli exec dir)
tautulli_data_location: "{{ tautulli_install_location }}/data"
```

## Dependencies

None

## Example Playbook

Install tautulli with the default settings
```yaml
- hosts: all
  roles:
     - role: wilmardo.tautulli
```

## License

BSD-3-Clause-Clear

## Author Information

This role was created in 2018 by [Wilmar den Ouden](https://wilmardenouden.nl).
