# common

Common server configuration

## Requirements

Works on ubuntu.

## Role Variables

* `dev_ops_keys` - An array of authorized keys
* `motd_title` - A message displayed at login

## Dependencies

Uses `ANXS.hostname` to set the hostname.

## Example Playbook

Here is an example configuration:

    - hosts: appservers
      roles:
        - { role: thermistor.common, motd_title: 'Hello there' }

## License

Licensed under the MIT License. See the LICENSE file for details.
