# common

Common server configuration

## Requirements

Works on ubuntu.

## Role Variables

* `dev_ops_keys` - An array of authorized keys for ssh
* `motd_title` - A message displayed at login

## Example usage

In a playbook:

    - hosts: appservers
      roles:
        - role: thermistor.common
          motd_title: 'Hello there'
          dev_ops_keys:
            - "{{ lookup('file', 'files/ssh_keys/yourkey.pub') }}"

## License

Licensed under the MIT License. See the LICENSE file for details.
