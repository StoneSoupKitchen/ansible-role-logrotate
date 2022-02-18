[![CI](https://github.com/StoneSoupKitchen/ansible-role-logrotate/actions/workflows/ci.yml/badge.svg)](https://github.com/StoneSoupKitchen/ansible-role-logrotate/actions/workflows/ci.yml)

# Ansible role: logrotate

An Ansible role for configuring logrotate.

## Requirements

Supported operating systems:
* Debian 10 (Buster)
* Debian 11 (Bullseye)

## Role Variables

The following table lists all variables that can be overridden
and their default values.

| Name                     | Default Value | Description                      |
| ------------------------ | ------------- | -------------------------------- |
| `logrotate_package` | systemd-journal-remote | Name of the logrotate package. Use `name=ver` format to pin. |
| `logrotate_package_state` | present | Installation state for the logrotate package. |

## Examples

```yaml
- hosts: all
  roles:
    - stonesoupkitchen.logrotate
```

## Development

A Makefile is included for easier development with `pipenv`.
After cloning this repository,
use the following commands to set up an environment.

    pipenv install --dev

To lint your changes with ansible-lint:

    make lint

To run tests with molecule:

    make test

## License

See [LICENSE](./LICENSE).

